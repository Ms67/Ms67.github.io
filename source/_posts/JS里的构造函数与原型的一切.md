
---
title: JS构造函数
date: 2022-4-22 23:00:01
---
1.构造函数 -->**类** Fn

```JavaScript
function Fn(){
}
```


2.原型(prototype) -->一个**对象**,也是**构造函数的一个属性**,用于存放类方法和类属性

```JavaScript
Fn.prototype.skill=functionsayHi(){        //Fn.prototype = {}
consolo.log('hi')
}
```
3.对象原型(_proto_)-->**实例对象**里存的一个**属性**,指向构造函数的原型.(形成原型链,实现继承)
```JavaScript
a = new Fn()
a._proto_=== Fn.prototype    //True     
```
4.构造函数 (construter) -->**prototype 里**的一个**属性**,值为'Fn'.用于**手动指定**实例对象的构造函数

5.原型链
由于 Fn.prototype也是一个对象,**也有_proto_属性**,所以当一个对象在构造函数的prototype里也找不到对应的方法的时候,可以沿着prototype的_proto_这一属性向上查找.这就叫原型链

原型链常用于给包装类型添加另外的方法

```JavaScript
String.prototype.reverse=function(){
	return this.split().reverse.jion('')
}

a = 'hello'
a.reverse()  //输出 'olleh'


```
