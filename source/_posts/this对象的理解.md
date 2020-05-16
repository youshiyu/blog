---
title: this对象的理解
date: 2020-03-30 21:18:33
tags:
---

## 普通函数中的this

this是函数 **运行时** 自动生成的一个内部的对象，总是指向调用它的对象

<p>//code here</p>

    var a=1;
	function foo()
    { 
    console.log(this.a)
    }
    foo() //1, 此时this指向window

--------------------------	
	const obj =  {
    name:'youshiyu',
    getname:function f() 
    {
        console.log(this.name) //普通函数this指向
    }
	}
	obj.getname() //谁调用了函数，谁就是this，这里很显然时obj
 	
---------------------------
## 作为构造函数的调用 
	
	
//如果出现了new,this将指向新new出来的对象

	function person() {
    return new person.prototype.init();
	}
	person.prototype = {
    init: function() {
        return this.name;
    },
    name: 'youshiyu'
	};
	console.log(person().name); /undefined

//详细解释这个例子:考察this指向，new方式，this绑定的是new出来的对象，此例中绑定的是person.prototype.init()，而init属性中没有name,name在原型person中
	
 
----------------------------



## 箭头函数中的this ##
	
### 

- 箭头函数中的this是通过继承得到的，本身没有this，指向最近一层非箭头函数的对象，如果要判断this就要看上一层对象的this指向谁。

- 注意：箭头函数只能用赋值式写法，不能用声明式写法,也就是建议不能直接作为对象的方法来使用 



     
   


    
	


	


