---
title: promise
date: 2020-05-15 22:39:38
tags:
---
#### promise ####
    promise构造函数是同步执行的，.then的函数时异步执行的。

    promise有三种状态pending,fulfilled,rejected。状态一旦改变不能再变,构造函数中只有第一次执行的resolve或reject第一次执行有效，多次调用没用。

    promise可以链式调用，每次调用返回.then或者.catch都返回一个新的promise
    
    
