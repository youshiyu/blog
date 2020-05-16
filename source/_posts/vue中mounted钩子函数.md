---
title: vue中mounted钩子函数
date: 2020-04-22 16:44:30
tags:
---


### mounted()中的this ###

    在mounted()钩子函数中，this指向的是windows作用域，当使用箭头函数的时候，会出现找不到data中的数据，将=>改成function(),就会指向Vue
