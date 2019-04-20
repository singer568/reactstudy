#### 1、全局安装webpack
     npm install webpack --global
#### 2、全局安装webpack-cli
     npm install webpack-cli --global
#### 3、创建工程002-webpack-demo并初始化  
1) 执行`npm init` 初始化工程，生成package.json
2) 执行`npm install webpack --save-dev`，本地安装webpack，并保存到依赖中去
3) 执行`npm install webpack-cli --save-dev`，安装webpack-cli，并保存到依赖中去
4) package.json文件内容如下：
```
   {
     "name": "002-webpack-demo",
     "version": "1.0.0",
     "description": "002-webpack-demo",
     "main": "index.js",
     "scripts": {
          "test": "echo \"Error: no test specified\" && exit 1"
     },
     "author": "singer568",
     "license": "ISC",
     "devDependencies": {
          "webpack": "^4.30.0",
          "webpack-cli": "^3.3.0"
     }
  }
```
####4、创建src文件夹
####5、在主目录下新建index.html，src文件夹下新建index.js，将来webpack打包后生成的目标js为main.js，生成到dist目录下
####6、执行`webpack --mode development`，在dist文件夹下生成main.js
####7、用浏览器打开index.html显示hello ~~
####8、在package.json文件中添加script命令
     "scripts": {  
          "dev": "webpack --mode development",  
          "build": "webpack --mode production"  
     }
####9、最终的package.json内容如下：
     {
  "name": "002-webpack-demo",
  "version": "1.0.0",
  "description": "002-webpack-demo",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "dev": "webpack --mode development",
    "build": "webpack --mode production"
  },
  "author": "singer568",
  "license": "ISC",
  "devDependencies": {
    "webpack": "^4.30.0",
    "webpack-cli": "^3.3.0"
  }
}

####9、执行`npm run dev` 即可完成打包