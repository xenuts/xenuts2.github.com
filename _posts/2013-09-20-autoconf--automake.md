---
layout: post
title: "Autoconf + automake的使用例解"
description: ""
category: programming
tags: [autoconf, automake, 编程, programming]
---
{% include JB/setup %}

* 建立一个hello world的C项目,目标执行程序为helloworld
#### main.c
{% highlight c %}
#include <stdio.h>
#include "myfunc.h"
int main(int argc, char** argv)
{
    int a = 1;
    printf ("%s %d\n","Hello World", a+func(10));
    return 0;
}
{% endhighlight %}

#### myfunc.c
{% highlight c %}
#include <stdio.h>
#include "myfunc.h"
int func(int a)
{
    return a * a;
}
{% endhighlight %}

#### myfunc.h
{% highlight c %}
int func(int a);
{% endhighlight %}

* 在当前目录下执行autoscan，扫描目录下源码，生成configure.scan。重命名configure.scan为configure.in，并做部分修改。
#### configure.scan
{% highlight bash %}
#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.
AC_PREREQ([2.68])
AC_INIT([FULL-PACKAGE-NAME], [VERSION], [BUG-REPORT-ADDRESS])
AC_CONFIG_SRCDIR([main.c])
AC_CONFIG_HEADERS([config.h])
# Checks for programs.
AC_PROG_CC
# Checks for libraries.
# Checks for header files.
# Checks for typedefs, structures, and compiler characteristics.
# Checks for library functions.
AC_OUTPUT
{% endhighlight %}

修改为（红色部分）：
#### configure.in
{% highlight bash %}
#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.
AC_PREREQ([2.68])
AC_INIT([helloworld], [1.0], [xiangzengzhou@gmail.com])
AC_CONFIG_SRCDIR([main.c])
AC_CONFIG_HEADERS([config.h])
AM_INIT_AUTOMAKE(helloworld,1.0)
# Checks for programs.
AC_PROG_CC(gcc)
# Checks for libraries.
# Checks for header files.
# Checks for typedefs, structures, and compiler characteristics.
# Checks for library functions.
AC_OUTPUT(Makefile)
{% endhighlight %}

* 执行aclocal生成aclocal.m4

* 执行autoconf生成configure

* 执行autoheader生成config.h.in

* 手工编写Makefile.am，例如下面内容

#### Makefile.am
{% highlight bash %}
AUTOMAKE_OPTIONS=foreign
bin_PROGRAMS=helloworld
helloworld_SOURCES=main.c myfunc.c myfunc.h
{% endhighlight %}
执行automake –add-missing根据Makefile.am生成Makefile.in
* 执行./configure生成makefile

* 执行make，编译项目生成目标执行程序helloworld

* 执行程序./helloworld

![Alt text](autoconf.jpg)

