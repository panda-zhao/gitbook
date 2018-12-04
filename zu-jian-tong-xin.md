# 父组件和子组件的通信

## 一 父组件给子组件传值

* 子组件在props中创建一个属性，用以接收父组件传过来的值
* 父组件中注册子组件
* 在子组件标签中添加子组件props中创建的属性
* 把需要传给子组件的值赋给该属性

【子组件】

```
<template>
<div>{{FatherToChild}}</div>
</template>
<script>
export default {
props:['FatherToChild'],// 创建props属性,通过父组件改变值
}
</script>
```

【父组件】

```
<template>
  <div>
    <ChildDemo :FatherToChild="msg"></ChildDemo>
  </div>
</template>
<script>
    import ChildDemo from "@/components/child.vue"
  export default {
    components: { 
      ChildDemo
    },
    data(){
      return{
        msg: "hello world!"
      }
    }
  }
</script>
```

## 二 子组件传递给父组件

总结一下：

* 子组件中需要以某种方式例如点击事件的方法来触发一个自定义事件
* 将需要传的值作为$emit的第二个参数，该值将作为实参传给响应自定义事件的方法
* 在父组件中注册子组件并在子组件标签上绑定对自定义事件的监听

【子组件中】

```
<template>
  <button @click="handleSubmit">向父元素传值</button>
</template>
<script>
  export default {
    props:['FatherToChild'],// 创建props属性,通过父组件改变值
    methods:{
      handleSubmit(){
        this.$emit("change","这条信息是从子组件传递的");//传递信息
      }
    }
  }
</script>
```

【父组件中】

```
<template>
  <div>
    <ChildDemo @change="handleChange"></ChildDemo>
  </div>
</template>
<script>
  import ChildDemo from "@/components/child.vue"
  export default {
    components: { 
      ChildDemo
    },
    methoss:{
      handleChange(data){
        console.log(data);
      }
    }
  }
</script>
```



