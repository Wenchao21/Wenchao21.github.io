---
layout: post
title: Python中的super
date:   2017-3-2
---

#### **反正一句话： 不要一说到 super 就想到父类！super 指的是 MRO 中的下一个类！**

首先必须要理解MRO

其次再去理解多继承

再次要去理解新式类

最后在做一下实践，才能理解super


```python

#先说一点：如果是我写，坚决不用super了，我更想用类名加方法名去调用，这样我认为是最直接的，知道哪个类里面的方法。

#切记一个人的代码不要两者混用，到时候自己都搞不清楚。



class Child(Parent):
      def __init__(self):
            Parent.__init__(self)


class Child(Parent):
      def __init__(self):
            super(Child, self).__init__(self)


#上述两段代码有什么区别吗？嘿嘿，应该是没有区别，一点区别都没有！这个是最简单的继承，如果类之间的继承复杂起来了呢？


#既然没有区别，那么为什么还要用super呢？看下面的代码

#首先必须要理解MRO

#其次再去理解多继承

#再次要去理解新式类

#最后在做一下实践，才能理解super


#总结一下： 直接用类名加方法名去调用，显示更直接，也更方便方法的查找，如果用super，这里就是关键了，super在调用的时候，是MRO的顺序来寻找方法的，不一定是父类的方法。

#不行了，越说越多了，已经讲不完了。今天先写到这里，后面再补充。先抄上知乎上的一段话，讲的很不错。

#不要一说到 super 就想到父类！super 指的是 MRO 中的下一个类！

      


class D(object):
    pass
 
class E(object):
    pass
 
class F(object):
    pass
 
class C(D, F):
    pass
 
class B(E, D):
    pass
 
class A(B, C):
    pass
 
if __name__ == '__main__':
    print A.__mro__


(<class '__main__.A'>, <class '__main__.B'>, <class '__main__.E'>,
 <class '__main__.C'>, <class '__main__.D'>, <class '__main__.F'>,
 <type 'object'>)





```