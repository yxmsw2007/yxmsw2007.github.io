---
layout: post
title: C语言设计模式-继承、封装和多态
comments: true
category: C/C++
tags: [设计模式, 继承, 封装, 多态]
---

## 前言

代码写的多了，也就越来越体会到设计模式的重要性，尤其是构建软件架构的时候，一个好的架构能减少大量的工作；

另外学会了设计模式也能更好的理解大牛们写的代码，而不至于拿到好项目的源码却无从下手；

所以学好设计模式极其重要，下面参考网上的文章结合自己的理解说说C语言中如何使用设计模式；

下面就说说面向对象的三个重要属性。

## 继承性 

继承是指这样一种能力：它可以使用现有类的所有功能，并在无需重新编写原来的类的情况下对这些功能进行扩展。

其继承的过程，就是从一般到特殊的过程。

```c

typedef struct _parent
{
    int data_parent;
    
}Parent;

typedef struct _Child
{
    struct _parent parent;
        int data_child;
        
}Child;

```

在设计C语言继承性的时候，我们需要做的就是把基础数据放在继承的结构的首位置即可。这样，不管是数据的访问、

数据的强转、数据的访问都不会有什么问题。

## 封装性

封装可以隐藏实现细节，使得代码模块化；封装是把过程和数据包围起来，对数据的访问只能通过已定义的界面。

面向对象计算始于这个基本概念，即现实世界可以被描绘成一系列完全自治、封装的对象，这些对象通过一个受

保护的接口访问其他对象。在面向对象编程上可理解为：把客观事物封装成抽象的类，并且类可以把自己的数据

和方法只让可信的类或者对象操作，对不可信的进行信息隐藏。

```c

struct _Data;

typedef void (*process)(struct _Data* pData);

typedef struct _Data
{
    int value;
    process pProcess;
}Data;

```

封装性的意义在于，函数和数据是绑在一起的，数据和数据是绑在一起的。这样，我们就可以通过简单的一个结构

指针访问到所有的数据，遍历所有的函数。封装性，这是类拥有的属性，当然也是数据结构体拥有的属性。

## 多态

多态性（polymorphisn）是允许你将父对象设置成为和一个或更多的他的子对象相等的技术，赋值之后，父对象

就可以根据当前赋值给它的子对象的特性以不同的方式运作。简单的说，就是一句话：允许将子类类型的指针赋

值给父类类型的指针。

```c

typedef struct _Play
{
    void* pData;
    void (*start_play)(struct _Play* pPlay);
}Play;

```

## 源码下载

[SampleC-CPP](https://github.com/yxmsw2007/SampleC-CPP.git)

## 参考资料

[C语言和设计模式（继承、封装、多态）](http://blog.csdn.net/feixiaoxing/article/details/7192302)
