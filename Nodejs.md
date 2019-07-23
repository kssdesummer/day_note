# Nodejs

### Node.js 和 npm 的安装

1. node.js下载地址：https://nodejs.org/en/
2. 在文件夹直接解压或者用`tar -zxvf 压缩包`
3. 在解压文件里找到node和npm位置：`bin`目录下面
4. 将node和npm链接到全局符号：
   1.  `sudo ln -s 全路径/node /usr/bin/node`
   2. `sudo ln -s 全路径/npm /usr/bin/npm`

5. 在任意目录下使用`node -v`或者`npm -v` 就可以看到相关版本号
6. 安装完成

### node程序

​	1. 在js文档的第一行总是写上`use strict`; 表明这是一个js代码

2. 在js文件中想要查看的结果用`console.log("hello world")`
3. `node --use strict hello.js`使用严格模式

### 搭建Node开发环境

​	推荐使用 visual studio code

### 模块

```javascript
hello.js
function greet(){
	console.log("1");//在终端控制台显示输出
	}
module.export = greet;	//将greet函数声明出去，别的模块也可以使用

main.js
var greet =require('./hello');	//使用时只需要再次声明，并且要加上该模块的路径和名字
```

### CommonJS规范

​	定义就是各个模块间的变量互不影响，想要使用别的模块的变量，就需要用moudule.export和require来传输和接受

### fs模块

​	fs：是Node.js的模块，负责读写文件(同步或异步)

 1. 读文件

     1. 异步：

        `fs.readFile('111.txt','utf-8',function(err,data){});`

    2. 同步：

       `var data = fs.readFileSync('sample.txt', 'utf-8');`

2.  写文件

   1. 异步：

      `fs.writeFile('output.txt',data,function(err){});`

   2. 同步：

      `fs.writeFileSync('output.txt', data);`

3. 查看文件信息

   1. `fs.stat('output.txt',function(err,stat){});`

### stream 模块

​	输入输出流

```javascript
'use strict';
var fs = require('fs');
var rs = fs.createReadStream('sample.txt');
var ws = fs.createWriteStream('copied.txt');
rs.pipe(ws);
//readable.pipe(writable, { end: false });
//rs.pipe(ws,"end:false");//设置write输入流执行完不结束
```

### http模块





