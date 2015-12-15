# animate
animate动画效果demo
animate.css是一款集视觉炫酷，动感活泼的效果与一体的跨浏览器动画库，是在项目中浓墨重彩的一笔。
在突出重点，主页，焦点图等制作上会有使人瞠目结舌的效果哦~

官方的演示以及下载地址：http://daneden.github.io/animate.css/

##兼容性
浏览器兼容：只兼容支持 CSS3 animate 属性的浏览器，他们分别是：`IE10+、Firefox、Chrome、Opera、Safari`。
##样例
###基本用法
* 在文档中添加样式文件，如下：

```javascript
 <head>
 <link rel="stylesheet" href="animate.min.css">
</head>
```
* 在你想要呈现动画效果的元素上添加`animated`样式名，若想要让动画无限循环，则可以在该元素上添加`infinite`样式名。
* 最后，你需要再添加以下其中一个样式名实现动画：

```javascript
flash
pulse
rubberBand
shake
headShake
swing
tada
wobble
jello
bounceIn
bounceInDown
bounceInLeft
bounceInRight
bounceInUp
bounceOut
bounceOutDown
bounceOutLeft
bounceOutRight
bounceOutUp
...（以下几十种省略）
```
###写法样例

```javascript
<h1 class="animated infinite bounce">Example</h1>
```
`animated` 类似于全局变量，它定义了动画的持续时间；`bounce` 是动画具体的动画效果的名称，你可以选择任意的效果。
具体动画可看上一级中的官方演示地址。
##具体用法
* 要在您的网站中使用animate.css,只需样式表放到您的文档中，并添加动画的元素，和任何动画名称的类。就是这个!赞赞赞!

```javascript
<head>
 <link rel="stylesheet" href="animate.min.css">
</head>
```
* 你也可以通过 `JavaScript` 或 `jQuery` 给元素添加这些 `class`，比如：

```javascript
$('#yourElement').addClass('animated bounceOutLeft');
```
* 你也可以检测一个动画结束时:

```javascript
$('#yourElement').one('webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend', doSomething);
```
* 有些动画效果最后会让元素不可见，比如淡出、向左滑动等等，可能你又需要将 `class `删除，比如：

```javascript
$(function(){
    $('#yourElement').addClass('animated bounce');
    setTimeout(function(){
        $('#yourElement').removeClass('bounce');
    }, 1000);
});
```
注: `jQuery.one()`是被选元素附加一个或多个事件处理程序，并规定当事件发生时运行的函数。当使用 one() 方法时，每个元素只能运行一次事件处理器函数。
* 你可以更改你的动画的持续时间，添加延迟或更改它播放次数:

```javascript
#yourElement {  
    -vendor-animation-duration: 3s;  /*持续时间*/
    -vendor-animation-delay: 2s; /*延迟时间*/ 
    -vendor-animation-iteration-count: infinite;/*播放次数*/
}
```
`特别要注意添加浏览器前缀噢。`
##demo
 [点击这里查看demo效果哦~](http://192.168.14.97:8080/acc/lxj/animate/animate.html)
##方法和API
* Animate.css主要是Grunt，你可以很轻松地创建自定义生成。首先，你需要Grunt和所有其他依赖项:

```javascript
$ cd path/to/animate.css/
$ sudo npm install
```
* 接下来运行`grunt watch`，更改配置，例如你只想要`attention seekers`里的部分动画，可以简单的编辑`animate-config.json`文件选择你需要的动画效果：
```javascript
"attention_seekers": {
  "bounce": true,
  "flash": false,
  "pulse": false,
  "shake": true,
  "headShake": true,
  "swing": true,
  "tada": true,
  "wobble": true,
  "jello":true
}
```
##更新日志
2015.12.15最新上传，无改动
