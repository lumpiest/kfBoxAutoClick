# kfBoxAutoClick
KF盒子点击

// ==UserScript==
// @name        kf auto click box
// @namespace   name space
// @description kf 自动点击盒子
// @include     http://bbs.2dgal.com/kf_smbox.php
// @version     1
// @grant       none
// ==/UserScript==
var myListItems = document.getElementsByClassName('box1');
var limitedList = myListItems[0].getElementsByTagName('a');
//console.log(myListItems);
console.log(limitedList);
//var x = document.getElementById("td").length;//.getElementsByTagName("P")
console.log(limitedList.length);
var x = Math.random(); //生成0-1中间的随机数
x = Math.ceil(Math.abs(x) * limitedList.length) //生成1-limitedList.length（还没有点击的盒子数目）中的随机数
console.log(limitedList[x]);
var y = new String();
y = limitedList[x];
console.log(typeof (y)); //艹y为什么不是string
//console.log(y.toString());
y = y.toString(); //转换Object to String
//y=y.slice(9,-2);//直接看会有多余的HTML标记
console.log(y);
location.replace(y); //网页重定向
