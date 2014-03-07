---
layout: post
title: "搭建Docear+Zotero+Chrome协作系统"
description: "Working with Docear + Zotero + Chrome"
category: 
tags: [Docear, Zotero]
---
{% include JB/setup %}

Docear 和 Zotero可以同时工作在Windows和Linux平台下，并结合Chrome浏览器使用，是一个很不错的学术管理框架。
Docear和Zotero都是可以跟远端同步备份，所以需要各自注册一个账户。

### 1. 安装Zotero及其相关插件
#### A. 安装Zotero
在https://www.zotero.org/download/可以在不同平台下的不同版本。因为我要和Chrome结合使用，因此选择Zotero Standalone和Chrome插件。Zotero Standalone解压即可，启动文件是run_zotero.sh（可能需要chmod +x），为了方便启动可以使用ln -s指令为启动文件在桌面上建立一个符号链接。Zotero的chrome插件会自动跳转到google的appstore进行安装，这样在使用chrome浏览一些例如google scholar等学术搜索时，就会在地址栏的右边显示出可以使用zotero的标志，可以将你感兴趣的文献导入到zotero中，so 方便啊！！！

#### B. 配置Zotero
选择左上角的Gear Icon进入Perferences：

1. Sync选项卡：首先登录自己的账户以便可以在远端备份本地数据和多机器间共用。此外由于远端服务器容量有限，上传文献的pdf文件是很不明智的选择，因此这里将File Syncing下的两个选项都去掉。
2. Advanced选项卡：在Files and Folders下设置Base Directory和Data Directory到你想要存放数据的位置，最好两个都设置在同一个路径下以方便管理。这里有一个技巧了：如果在同一台机器上的Linux和Windows系统下如何共用一个数据库呢，就是将这两个路径设置在Window盘下，这样在Linux下挂载这个盘并设置同样的路径就可以共享数据和附件了，大大方便了双系统间的合作，也不用将pdf附件等在远端同步了。
3. Bibtex格式设置：Zotero可以导出丰富的格式，当然包括Bibtex和BibLatex格式了，默认的Zotero设置bibtex和biblatex中的关键词为"$Author\_$title首单词\_$year"，我比较喜欢的格式是"$Author:$year:$title首单词"，修改的方法是打开Data Directory下的translator文件夹下的bibtex.js和biblatex.js文件中的var citeKeyFormat = "%a:%y:%t"即可。

#### C. 安装Autozotbib
Autozotbib是Zotero的一个插件，可以自动地将Zetoro的添加/删除/更新等操作实时的反映到指定的导出文件（使用firefox的可以使用类似的插件Zotero Autoexport）。从网站http://www.rtwilson.com/academic/autozotbib上可以下载一个xpi格式的文件，然后使用Zotero->Tools->Add-ons导入该文件进行安装，重启Zotero即可。重启后，在Zotero的Gear Icon下会多出两个AutoZotib的选项，进入AutoZotBib Perferences设置需要导出的bib文件的路径和位置，最好放在Zotero的Base Directory中方便管理，这个实时更新的bib文件就可以被Docear使用，参看下文。


### 2. 安装Docear
在https://www.docear.org/software/download/可以下载到Windows/Linux/Mac OS平台下的Docear的安装包。
Windows平台下按默认的安装流程就可以了；
Linux下解压即可使用，启动文件为docear.sh（可能需要chmod +x），为了方便启动可以使用ln -s指令为启动文件在桌面上建立一个符号链接。

#### A. 配置Docear
1. 登录自己的账户：进入perferences -> Online Services -> Docear Account -> Login
2. 首先建立一个新的project（或者打开一个已经存在的project）：在左边panel的根节点上右键选择New Project，主要注意Project Home的设置
3. 在左边Panel中右击References->Change Reference Database设置为上文AutoZotBib Perference设置的导出文件即可。
