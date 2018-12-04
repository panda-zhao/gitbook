CSS 中文：指层叠样式表 英文：Cascading Style Sheets  
HTML定义文档内容，样式表定义如何显示 HTML 元素。为了解决内容与表现分离的问题，万维网联盟（W3C）在 HTML 4.0 之外创造出样式（Style）。外部样式表使你有能力同时改变站点中所有页面的布局和外观。

## CSS语法

```js
/*这是一个注释*/
selector{property:value;property:value;}
```

**【语法】  **  
1. CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:  
2. 选择器通常是您需要改变样式的 HTML 元素。  
3. 每条声明由一个属性和一个值组成。  
4. 属性（property）是您希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开。  
5. CSS声明总是以分号\(;\)结束。  
6. 声明组以大括号\({}\)括起来。  
7. 注释是用来解释你的代码，并且可以随意编辑它，浏览器会忽略它。CSS注释以 "/" 开始, 以 "/" 结束。
