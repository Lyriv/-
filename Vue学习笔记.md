## vue学习笔记

### 一，vue的项目搭建

- 安装node环境和npm环境


- 配置环境变量
  - 用户变量：D:\Develop\nodejs\node_modules
    - NODE_PATH
  - 系统变量 ：D:\Develop\nodejs;D:\Develop\nodejs\node_global
    - path
- 检测是否安装成功
  - node -v
  - npm -v
- 安装cnpm
  - npm install -g cnpm –registry=https://registry.npm.taobao.org
  - 同样使用 cnpm 来确认是否安装成功

### 二，搭建vue项目环境和项目

- 安装 vue-cli  
  - cnpm install vue-cli -g  全局安装vue-cli
  - 使用vue list来查看是否安装成功
- 在项目的目录中使用命令 vue init webpack + 项目名称  创建一个基于脚手架的vue项目
  - Vue build ==> 打包方式
  - Install vue-router ==> 是否要安装 vue-router，项目中肯定要使用到 所以Y 回车；
  - Use ESLint to lint your code ==> 是否需要 js 语法检测 
  - Set up unit tests ==> 是否安装 单元测试工具
  - Setup e2e tests with Nightwatch ==> 是否需要 端到端测试工具
- 进入项目之后使用 cnpm -install来安装依赖
  - 安装的依赖在node_modules
- 最后通过 npm run dev 启动项目
- 进入 http://localhost:8080/  就可以打开项目

### 三，前端常用插件

- vscode
  -  **Auto Close Tag**    自动闭合HTML/XML标签
  -  **Auto Rename Tag **  自动完成另一侧标签的同步修改
  -  **Beautify**  **格式化 html ,js,css**
  -  **Bracket Pair Colorizer**  给括号加上不同的颜色，便于区分不同的区块，使用者可以定义不同括号类型和不同颜色
  -  **GitLens**  方便查看git日志，git重度使用者必备
  -  **HTML CSS Support **  智能提示CSS类名以及id 
  -  **HTML Snippets **  智能提示HTML标签，以及标签含义
  -  **JavaScript(ES6) code snippets **  ES6语法智能提示，以及快速输入，不仅仅支持.js，还支持.ts，.jsx，.tsx，.html，.vue，省去了配置其支持各种包含js代码文件的时间
  -  **Markdown Preview Enhanced**  实时预览markdown，markdown使用者必备
  -  **Vetur** Vue多功能集成插件，包括：语法高亮，智能提示，emmet，错误提示，格式化，自动补全，debugger。vscode官方钦定Vue插件，Vue开发者必备。
  -  VueHelper  vue代码片段
  -  **Dracula Official**  很好看的一款主题风格

### 四，vue的项目结构

```
├── index.html                      入口页面
    ├── build                           构建脚本目录
    │   ├── build-server.js                 运行本地构建服务器，可以访问构建后的页面
    │   ├── build.js                        生产环境构建脚本
    │   ├── dev-client.js                   开发服务器热重载脚本，主要用来实现开发阶段的页面自动刷新
    │   ├── dev-server.js                   运行本地开发服务器
    │   ├── utils.js                        构建相关工具方法
    │   ├── webpack.base.conf.js            wabpack基础配置
    │   ├── webpack.dev.conf.js             wabpack开发环境配置
    │   └── webpack.prod.conf.js            wabpack生产环境配置
    ├── config                          项目配置
    │   ├── dev.env.js                      开发环境变量
    │   ├── index.js                        项目配置文件
    │   ├── prod.env.js                     生产环境变量
    │   └── test.env.js                     测试环境变量
    ├── mock                            mock数据目录
    │   └── hello.js
    ├── package.json                    npm包配置文件，里面定义了项目的npm脚本，依赖包等信息
    ├── src                             项目源码目录    
    │   ├── main.js                         入口js文件
    │   ├── app.vue                         根组件
    │   ├── components                      公共组件目录
    │   │   └── title.vue
    │   ├── assets                          资源目录，这里的资源会被wabpack构建
    │   │   └── images
    │   │       └── logo.png
    │   ├── routes                          前端路由
    │   │   └── index.js
    │   ├── store                           应用级数据（state）
    │   │   └── index.js
    │   └── views                           页面目录
    │       ├── hello.vue
    │       └── notfound.vue
    ├── static                          纯静态资源，不会被wabpack构建。
    └── test                            测试文件目录（unit&e2e）
        └── unit                            单元测试
            ├── index.js                        入口脚本
            ├── karma.conf.js                   karma配置文件
            └── specs                           单测case目录
                └── Hello.spec.js
```



## 项目实战

### 一,使用百度api进行地理位置的获取



