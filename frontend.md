title: Hey, 前端
speaker: 段宏
transition: move
files: /js/demo.js,/css/demo.css,/js/zoom.js
theme: moon

[slide data-transition="zoomin"]

# Hey, 前端

<small>speaker: duanhong</small>

[slide]

### 前端 = HTML + CSS + JavaScript   / + ??

[slide data-transition="kontext"]
一开始，前端是这样的 

``` html
<!DOCTYPE html>
<html>
    <head>
        <title>hello world</title>
        <style>
        <!-- some css rules here -->
        </style>
    </head>
    <body>
        <button id="hello-btn" class="btn btn-primary">Hey, gays and girls! </button>
        <script type="text/javascript">
            function sayHey() {
               alert('Heys, gays!');
            }
            document.getElementById('hello-btn').addEventListener('click', sayHey, false);
        </script>
    </body>
</html>
```

[slide]
## DEMO
------

<button class="btn btn-primary btn-block btn-lg" id="hello-btn">Hey, gays and girls</button>
<script type="text/javascript">
    function sayHey() {
       alert('Hey, gays and girls');
       this.textContent = '亲们, 给点掌声吧'; 
    }
    document.getElementById('hello-btn').addEventListener('click', sayHey, false);
</script>

[slide]
####有时候，会耍点小聪明
----
<iframe data-src="http://jsbin.com/sogehi/4/edit?html,css,output" src="about:blank;"></iframe>

[slide]

[前端还挺有趣的，是吧？](http://bartaz.github.io/impress.js/#/bored)

[slide data-transition="glue"]
## 保持一颗好奇心
![what instagram using](/imgs/instagram.png)


[slide]
## 慢慢的积累和沉淀的过程....

* 技术书籍
* 社区，论坛(博客园...)
* **Github** 

[slide]
#### 后来，这货出现了
--------
<iframe data-src="http://getbootstrap.com" src="about:blank;"></iframe>

[slide]
### 前端一下子热闹了好多
--------
[让我们来看一看](https://github.com/search?utf8=%E2%9C%93&q=stars%3A%3E10000&type=Repositories&ref=searchresults)

[slide data-transition="vertical3d"]
### 接着 各种框架，库，工具蜂拥而至
--------
* [Design essentials](https://github.com/showcases/design-essentials)
* [Clean code linters](https://github.com/showcases/clean-code-linters)
* [Front-end JavaScript frameworks](https://github.com/showcases/front-end-javascript-frameworks)
* [CSS preprocessors](https://github.com/showcases/css-preprocessors)
* [Icon fonts](https://github.com/showcases/icon-fonts)
* [Package managers](https://github.com/showcases/package-managers)

[slide]
### 作为伸手党, 我也是醉了
------
[一入前端深似海](https://github.com/JingwenTian/awesome-frontend)

[slide]
### 有时候吧，发现前端还是**挺容易的**
---------
* 问题 -> Github {:&.bounceIn}
* 需求 -> Github
* .... -> Github

* 这么多的资源在手，还愁做不出东西吗？

[slide]
### 积木的世界
--------
Bootstrap + jQuery/plugins (+ MVC frameworks)= Whatever

[slide]
###世界真美好
--------
    * 节省时间 {:&.fadeIn}
    * 兼容性好
    * 文档和资源丰富
    * 简单、易学

[slide]
#### 那么，问题来了
----------
* <label class="label text-danger">性能</label> {:&.fadeIn}
* <label class="label text-danger">可定制性 </label>
* <label class="label text-danger">更新维护 </label>
* <label class="label text-danger">...... </label>
* <label class="label text-primary">反思～</label>

[slide]
### 回归本质
---------
* 追本溯源 (HTML, JS, CSS) {:&.zoomIn}
    * HTML -> Markdown, Jade 
    * CSS -> LESS, SASS, Stylus 
    * JS -> CoffeeScript, ES6, TypeScript, Dart
* 提高效率，保证质量
    * Libs -> Zepto, jQuery, AngularJS, React
    * PackageManger -> npm, bower
    * Module -> AMD, CMD, CommonJS(seajs, requirejs, browserify)
    * Product -> Grunt, Gulp, Webpack
* 切忌（不要只停留在炫技和跟风阶段）

[slide]
### 适合自己的, 不断完善, 逐步跟进
---------
![my environment settings](/imgs/my.png)

[slide data-transition="zoomin"]
#### [关于React的那些事儿](http://facebook.github.io/react/index.html)
------
![about react](/imgs/react.png)

[note]
![react notion](/imgs/data_flow.svg)
[/note]

[slide]
#### 不得不提的Flux
--------
![react notion](/imgs/flex.png)

[slide]

![小萝莉](/girl.jpg "小萝莉")

[slide]

> Stay hungary , Stay Foolish 
    <small class="pull-right" style="margin-top: 30px;">Steve.Jobs</small>

[slide]
![payme](/imgs/payme.jpg)
