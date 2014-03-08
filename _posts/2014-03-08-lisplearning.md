---
layout: post
title: "Lisp学习"
description: ""
category:
tags: []
---
{% include JB/setup %}
## 选择Lisp的方言
中标者： Scheme

## 选择Scheme的实现
中标者：[Racket](http://racket-lang.org/)

## 集成到Emacs中
参见Racket的[manual](http://docs.racket-lang.org/guide/Emacs.html),使用到了两个插件[Quack](http://www.neilvandyke.org/quack/)和[Geiser](http://www.nongnu.org/geiser/)

+ 首先，安装Racket从[http://racket-lang.org/download/](http://racket-lang.org/download/)，因为Geiser要求Racket和Guile至少有一个被安装
+ Emacs自带了scheme-mode，可以使用`M-x scheme-mode`激活
+ 下载quack.el并放到Emacs的load-path下
+ 安装Geiser:如果是Emacs24以后的版本，可以使用ELPA([the Emacs Lisp Package Archive](http://www.emacswiki.org/emacs/ELPA))来安装，只需 `M-x package-install RET geiser RET`；或者自己下载源码安装，参见自带的INSTALL
+ Emacs配置和使用：
{% highlight scheme %}
(load "quack")
(setq geiser-active-implementations '(racket)) ;geiser默认使用Racket实现
(setq scheme-program-name "racket") ;M-x run-scheme时调用racket
{% endhighlight %}


当编辑*.scm文件时，进入scheme-mode（在菜单栏里可以看到geiser和quack, 使用`M-x run-geiser`目录为当前buffer开启REPL。


