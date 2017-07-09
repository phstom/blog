---
layout: post
title: python bool函数
categories: python
description: python
keywords: python
---

bool([x])

>英文说明：Convert a value to a Boolean, using the standard truth testing procedure. If x is false or omitted, this returns False; otherwise it returns True. bool is also a class, which is a subclass of int. Class bool cannot be subclassed further. Its only instances are False and True.
New in version 2.2.1.
Changed in version 2.3: If no argument is given, this function returns False.

>中文说明：将x转换为Boolean类型，如果x缺省，返回False，bool也为int的子类；
参数x：任意对象或缺省；大家注意到：这里使用了[x]，说明x参数是可有可无的，如果不给任何参数则会返回False。

bool()

    >>>bool(0)
    False
    >>>bool('abc')
    True
    >>>bool(' ')   #参数是一个空格，非空。
    True
    >>>bool('')    #参数为空。
    False
    >>>bool([])
    False
    >>>bool()
    False
    >>>bool(None)
    False
    >>>issubclass(bool,int) #bool是一个subclass int
    True

聪注：

>bool( )函数返回bool值

>可以用于判断是否为空，及判断输入是否为空。

>可用于密码输入判断

案例

    def volid(pwd):
        p = bool(pwd)  #判断是否为空，为空则返回False。这里应该在加一个判断pwd长度的函数。
        a = any(map(str.isupper,pwd))
        b = any(map(str.islower,pwd))
        c = any(map(str.isdigit,pwd))
        d = not all(map(str.isalnum,pwd))
        return all([p,a,b,c,d])

>这里的isupper islower isdigit isalnum 函数都很好理解，就是判断是不是大写，是不是小写，是不是数字，是不是全是数字和字母（反过来就是判断有没有其他符号），而这里的map函数就是把后面那个集合的每个元素用第一个参数的函数执行一遍，返回一个bool类型的集合，最外层的any和all函数就比较容易理解了，可以用“或”和“与”来理解，如果参数集合有一个为真，any函数就返回true，相当于把所有元素“或”一下，只有当参数集合全部为真，all函数才返回true,其他情况都是返回false ,所以如果volid函数传入一个包含大写小写字母数字和特殊符号的字符串后，abcd就被赋值为true，最后return true，所以这个函数就可以判断密码够复杂。

问题：

>上例中，如果要求四项中只需要满足两项，函数该怎么写比较简练。
参考资料：

[http://www.pythontab.com/html/2013/hanshu_0122/157.html](http://www.pythontab.com/html/2013/hanshu_0122/157.html)
[http://www.jb51.net/article/64516.htm](http://www.jb51.net/article/64516.htm)
