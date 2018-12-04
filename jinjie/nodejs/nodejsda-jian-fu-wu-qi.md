首先新建一个node文件夹，在文件夹内新建一个app.js文件

```js
var http = require("http");

var server = http.createServer(function(request,response){
  response.setHeader("Content-Type","text/plain;charset=utf-8");
  response.setHeader("Access-Control-Allow-Origin","*");
  response.setHeader("Access-Control-Allow-Headers","Origin, X-Requested-With, Content-Type, Accept");
  response.end("Node服务器运行成功！");
  console.log('数据发送成功！');
});

var port = 8888;
var host = "127.0.0.1";
server.listen(port,host,function(){
  console.log('Server running at http://'+ host + ':' + port)
});
```

然后在node文件夹内启动命令框，输入node app.js.  
此时我们在浏览器打开 [http://127.0.0.1:8888/](http://127.0.0.1:8888/，发现一个web服务器就建立成功了！) 发现一个web服务器就建立成功了！

