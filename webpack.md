title: webpack 介绍
speaker: 段宏
transition: move
files: /js/demo.js,/css/demo.css,/js/zoom.js
theme: moon

[slide data-transition="zoomin"]

# Webpack 介绍

<small>speaker: duanhong</small>

[slide]

## 网页 -> 网页应用   
-----------------

*  JS 多 & 复杂 {:&.fadeIn}
*  越来越多的逻辑处理转移到浏览器端(SPA, 富应用)
*  整页的刷新和重载越来越少（ajax,pjax,...） 

[slide data-transition="kontext"]
## 维护和优化代码？  
-----------
*  组件化 {:&.fadeIn}
*  模块化 
*  工程化

[slide]
## 现存的模块管理  
----------

*  `<script>` 罗列标签  {:&.fadeIn}
*  CommonJs -> nodejs, browserify, webpack
*  CMD -> seajs
*  AMD -> requirejs, webpack

[slide]
##  罗列标签  

----
``` JavaScript
    <script src="module1.js"></script>
    <script src="module2.js"></script>
    <script src="libaryA.js"></script>
    <script src="module3.js"></script
```

[slide]
## 诸多问题  
-----------

* 全局对象易发生污染  {:&.fadeIn}
* 加载顺序没法保证 
* 依赖关系没法维护
* 第三方类库的引入
* 难以用于大型项目

[slide]
## CommonJS
[note]
CommonJS组织定义了该规范，通过把JS的执行限制在自己的命名空间里解决了JS作用域的问题。  
[/note]

* 需要那些依赖 (require) {:&.fadeIn}
* 对外提供什么服务 (module.exports)

[slide]
### CommonJs: DEMO
---------------
``` JavaScript  

    require("module");
    require("../file.js");
    exports.doStuff = function() {};
    module.exports = someValue;

```

[slide data-transition="glue"]
## 优点
--------
* 易用 {:&.fadeIn}
* 重用(nodejs)
* 丰富的组件生态(npm) 

[slide data-transition="glue"]
## 缺点
--------
* 不支持模块的懒加载(异步加载) {:&.fadeIn}
* 不支持多模块的并行引入

[slide]
## CommonJS 实现
------

* node.js [server-side]
* browserify


[slide]
## AMD: 异步模块加载
[note]
AMD的产生源自于CommonJS的非异步,它定义了模块的异步加载规范，解决了异步加载的问题
[/note]

-----------------
``` JavaScript
    require(["module", "../file"], function(module, file) { /* ... */ });
    define("mymodule", ["dep1", "dep2"], function(d1, d2) {
      return someExportedValue;
    });
```
[slide]
## AMD 优缺点
-----------
## 优点 

* 符合浏览器端资源的异步加载模式
* 支持多模块的并行加载

## 缺点  

* 依赖模块单独编写 (去掉后倒显得不错)
* 越来越难以阅读和理解 (模块名称的定义)
* 只是一种解决问题的方法 

[slide]
## AMD 实现  
----------
* require.js
* curl - client-side

[slide]
## 模块的下载

* 一个请求一个模块 {:&.fadeIn}
* 所有模块一个请求  
* 更好的做法...

[slide]
## 一个请求一个模块 
* 优点: 只加载需要的模块
* 缺点: 多请求，就意味着多延迟  

[slide]
## 所有模块一个请求 
* 优点: 少请求，少延迟
* 缺点: 非依赖模块的冗余加载

[slide]
## 分段传输 
----------
<p class="flexbox vleft">
对于大型网页应用来说，不能简单的把所有依赖的代码打包到一个文件里，特别是一些模块只有在特定场景下才会使用到。

那如何把代码拆分成按需加载的模块?  
</p>

*  合并公用组件 ? 
*  按需加载 ?

[slide]
编译模块的时候，按照依赖关系动态的进行打包和拆分  

* 依赖模块合并
* 非依赖模块按需加载    =>  更小的包，更少的请求数 => 更快的首页加载
* 大模块分拆

[slide]
## Webpack 功能？ 特性？

[slide]
## Webpack 深入
-------

*  [webpack is awesome](https://unindented.github.io/webpack-presentation/#/)
*  [manage front-end with webpack](http://peerigon.github.io/presentations/2014-07-09-MNUG-webpack/#1)

