---
layout: post
title: Object VS Function
---

### Problem in OOP

OOP programming language like Java face one problem. Everything is object. Even though sometime you just need one action, you must use object(class). Actually, all you need is just the method(function) in that class. The definition of the class is totally a waste of space.

### Solution in Java

To provide convinience for the situation we talked before, Java create Functional Interface. This interface only define one virtual method in it. This virtual method must be implemented by the class using this interface. So in functional interface, the focus change from class to method, i.e. function.

### Development in Java

Since all we care is the action, the name of the method is useless for us. Java provide Lambda expression to reach this goal. Instead of writing all the redundant class and method name, using () -> {} makes everything much tidier. To make this process more meaningful, using Function Reference is a better choice.

### Lambda Expression

Lambda expression is a syntax sugar in Java. Java compiler will translate lambda expression into anonymous inner class owning the same function. Syntax sugar does nothing to the running of program in JVM.
