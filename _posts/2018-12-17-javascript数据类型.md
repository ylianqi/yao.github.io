---
layout:     post
title:      javascript数据类型
subtitle:   javascript数据类型
date:       2018-12-17
author:     YAO
header-img: img/post-bg-cook.jpg
catalog: true
tags:
    - javascrip
---

## 数据类型分类和区别
### 分类
javascript数据类型分为：值类型（基本数据类型）、引用数据类型；
### 区别
#### 值类型
-  值类型是保存在栈内存中的简单数据段，栈内存提供了供js代码执行的环境；
- 值类型是对值的操作；
#### 引用数据类型
 - 引用数据类型是存放在堆内存中的对象，变量其实是保存在栈内存中的一个指针（保存的是堆内存的引用地址），这个指针指向堆内存；
- 引用数据类型是对地址的引用，当访问时，我们需要先从栈内存中读取内存地址，然后根据内存地址找到找到栈内存中的值
![栈内存、堆内存.jpg](https://upload-images.jianshu.io/upload_images/4804750-69d9d3904f9b2eed.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
## 值类型
值类型：Number、String、Boolean、Null、Undefined、Symbol（es6）
从一个变量向另一个变量复制时，会在栈中创建一个新值，然后把值复制给新变量，改变源数据不会影响新便变量
### Number 数字类型
```
let num1 = 123;
let num2 = num1;
console.log(num2);  //123
num1 = 321;
console.log(num1);  //321
console.log(num2);  //123
```
### String 字符串类型
```
let str1 = 'Hello';
let str2 = str1;
console.log(str2);  //Hello
str1 = 'World';
console.log(str1);  //World
console.log(str2);  //Hello
```
### Boolean 布尔值
Boolean类型只有两个值：true和false
### Null
Null是一个空置，表示一个空对象指针，用typeof检测得到“Object”；
可以通过将变量值的设置为null，来清空变量
### Undefined
Undefined表示未定义，代表声明了但没有定义
## 引用数据类型
引用数据类型：Object（js中除了基本数据类型都是对象，数据是对象，函数是对象，正则是对象，日期是对象...）
所以我们简单的把引用数据类型分为对象数据类型和函数数据类型；
对象数据类型包括：对象，数组，正则，日期对象等；
函数数据类似那个主要是指执行的函数，函数又分为两个部分：函数的定义阶段，函数调用阶段
## typeof检测
typeof有两种写法：typeof(xxx) 和 typeof xxx

```typeof(123)  //number
typeof('hello')  //string
typeof(true)  //boolean
typeof(undefined)  //undefined
typeof(null)  //object
typeof({})  //object
typeof([])  //object
typeof(function () {})  //function
```
 

