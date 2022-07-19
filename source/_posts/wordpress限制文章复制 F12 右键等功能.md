---
title: wordpress限制文章复制 F12 右键等功能
category: 
renderNumberedHeading: true
grammar_cjkRuby: true
tags: 'wordpress,F12'
---


# 教程

- 当下浏览器还是很多的，如果你想你的网站内容不被人手工采集的话，你的图片不想被人另存为或下载的话，我们完全可以禁止右键。
![enter description here](./images/20200919091823323-300x82_2.webp)

- 将以下代码复制主题文件 footer.php中即可！

``` javascript
<script type = ‘text/javascript’ >
//屏蔽右键菜单
document.oncontextmenu = function(event) {
if (window.event) {
event = window.event;
}
try {
var the = event.srcElement;
if (!((the.tagName == “INPUT” && the.type.toLowerCase() == “text”) || the.tagName == “TEXTAREA”)) {
return false;
}
return true;
} catch (e) {
return false;
}
}
//屏蔽粘贴
document.onpaste = function(event) {
if (window.event) {
event = window.event;
}
try {
var the = event.srcElement;
if (!((the.tagName == “INPUT” && the.type.toLowerCase() == “text”) || the.tagName == “TEXTAREA”)) {
return false;
}
return true;
} catch (e) {
return false;
}
}
//屏蔽复制
//屏蔽剪切
document.oncut = function(event) {
if (window.event) {
event = window.event;
}
try {
var the = event.srcElement;
if (!((the.tagName == “INPUT” && the.type.toLowerCase() == “text”) || the.tagName == “TEXTAREA”)) {
return false;
}
return true;
} catch (e) {
return false;
}
}
//禁止f12
function fuckyou() {
window.close(); //关闭当前窗口(防抽)
window.location = “about:blank”; //将当前窗口跳转置空白页
}
function ck() {
console.profile();
console.profileEnd();
//我们判断一下profiles里面有没有东西，如果有，肯定有人按<a href="https://www.902d.com/tag/288" title="【查看含有[F12]标签的文章】" target="_blank">F12</a>了，没错！！
if (console.clear) {
console.clear()
};
if (typeof console.profiles == “object”) {
return console.profiles.length > 0;
}
}
function hehe() {
if ((window.console && (console.firebug || console.table && /firebug/i.test(console.table()))) || (typeof opera == ‘object’ && typeof opera.postError == ‘function’ && console.profile.length > 0)) {
fuckyou();
}
if (typeof console.profiles == “object” && console.profiles.length > 0) {
fuckyou();
}
}
hehe();
window.onresize = function() {
if ((window.outerHeight – window.innerHeight) > 200)
//判断当前窗口内页高度和窗口高度，如果差值大于200，那么呵呵
fuckyou();
}
document.onkeydown = function(event) {
if ((event.keyCode == 112) || //屏蔽 F1
(event.keyCode == 113) || //屏蔽 F2
(event.keyCode == 114) || //屏蔽 F3
(event.keyCode == 115) || //屏蔽 F4
// (event.keyCode == 116) || //屏蔽 F5
(event.keyCode == 117) || //屏蔽 F6
(event.keyCode == 118) || //屏蔽 F7
(event.keyCode == 119) || //屏蔽 F8
(event.keyCode == 120) || //屏蔽 F9
(event.keyCode == 121) || //屏蔽 F10
(event.keyCode == 122) || //屏蔽 F11
(event.keyCode == 123)) //屏蔽 F12
{
return false;
}
}
window.onhelp = function() {
return false;
} </script>

```

- 这样就可以了，抓紧去看看你的网站好了吗？ 