---
layout: page
title: "Academic"
description: "Academic"
group: navigation
---
{% include JB/setup %}



## [Search]
[Google](http://www.google.com)
 | [百Google度](http://www.baigoogledu.com)
 | [Google Scholar](http://scholar.google.com/)
 | [IEEExplore](http://ieeexplore.ieee.org/Xplore/home.jsp)
 | [MS Academic Search](http://academic.research.microsoft.com/Default.aspx)
 | [ACM PKU](http://acm.lib.tsinghua.edu.cn/acm/)
 | [Wiley Online](http://onlinelibrary.wiley.com/)
 | [ScienceDirect](http://www.sciencedirect.com/)
 | [DBLP](http://www.informatik.uni-trier.de/~ley/db/) (Computer Science Bibliography)
 | [MedSci](http://www.medsci.cn/sciif.asp?action=search) (影响因子)
 | [SCI](http://www.thomsonscientific.com/cgi-bin/jrnlst/jlresults.cgi?PC=K) (Science Citation Index)
 | [SCIE](http://www.thomsonscientific.com/cgi-bin/jrnlst/jlresults.cgi?PC=D) (Science Citation Index Expanded)
 | [EI](http://www.engineeringvillage.com/search/quick.url)
 | [arXiv.org](http://arxiv.org/)
 | [Computer Science Bibliographies](http://liinwww.ira.uka.de/bibliography/index.html)
 | [ProQuest](http://search.proquest.com/index) (国外高质量学位论文全文的数据库)
 | [国家自然科学基金委员会](http://www.nsfc.gov.cn/Portal0/default152.htm)
 | [CALIS高校学位论文库](http://etd.calis.edu.cn/)

## [Academics]
[WikiCFP](http://www.wikicfp.com/cfp/)
 | [Citeulike](http://www.citeulike.org/home)
 | [NOW](http://www.nowpublishers.com/)
 | [BibSonomy](http://www.bibsonomy.org/)

### CV
[CVonline](http://homepages.inf.ed.ac.uk/rbf/CVonline/CVentry.htm)
 | [CVPapers](http://www.cvpapers.com/index.html)

## [English]
[沪江网](http://www.hujiang.com/en/#tabs_mainhearder)

### 词汇
[01-四级核心词汇](http://cichang.hujiang.com/book/10445)
 | [02-六级核心词汇](http://cichang.hujiang.com/book/10447)
 | [03-托福核心词汇](http://cichang.hujiang.com/book/10567)

### 听力
[01-慢速美音](http://app.hujiang.com/listen/mansu/?date=2013-02-26)
 | [02-标准美音](http://app.hujiang.com/listen/biaozhun/)

### 口语

### 阅读

## [Techniques]

### Python
[PyTech](http://hyry.dip.jp/tech/slice/slice.html/24)

### DeepLearning
[Deep Learning](http://deeplearning.net/)([tutorial](http://deeplearning.net/tutorial/contents.html), [Theano](http://deeplearning.net/software/theano/))<br>
[Deep Belief Networks资料汇总](http://fantasticinblur.iteye.com/blog/1131640)<br>
[Deep Learning Methods for Vision - CVPR 2012 Tutorial](http://cs.nyu.edu/~fergus/tutorials/deep_learning_cvpr12/)<br>
[LISA](http://www.iro.umontreal.ca/~lisa/twiki/bin/view.cgi/Public)<br>
[A Brief Introduction to Neural Networks - D. Kriesel](http://www.dkriesel.com/en/science/neural_networks)<br>

### MachineLearning
[Machine Learning Surveys](http://www.mlsurveys.com/)<br>
[MALLET](http://mallet.cs.umass.edu/index.php) - a Java-based package for statistical natural language processing, document classification, clustering, topic modeling, information extraction, and other machine learning applications to text.<br>
[STPRTool](http://cmp.felk.cvut.cz/cmp/software/stprtool/) - Statistical Pattern Recognition Toolbox for Matlab.<br>
[Spider](http://people.kyb.tuebingen.mpg.de/spider/) - a complete object orientated environment for machine learning in Matlab.<br>
[Maximum Entropy Modeling Toolkit for Python and C++](http://homepages.inf.ed.ac.uk/lzhang10/maxent_toolkit.html)<br>
[Shogun](http://www.shogun-toolbox.org/page/home/) - A Large Scale Machine Learning Toolbox.<br>
[MILK](https://github.com/luispedro/milk) - Machine Learning Toolkits in Python.<br>
[国际流行开源机器学习和模式识别工具](http://blog.csdn.net/tangyongkang/article/details/6143031)<br>


## Refs

Read [Jekyll Quick Start](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)<br>
Complete usage and documentation available at: [Jekyll Bootstrap](http://jekyllbootstrap.com)<br>
[Liquid](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers)<br>
[Markdown 语法说明 (简体中文版)](http://wowubuntu.com/markdown/#precode)<br>
[Jekyll 中的语法高亮：Pygments](http://havee.me/internet/2013-08/support-pygments-in-jekyll.html)<br>
[利用Jekyll搭建个人博客](http://www.mceiba.com/develop/jekyll-introduction.html)<br>
[写作环境搭建(git+github+markdown+jekyll)](http://site.douban.com/196781/widget/notes/12161495/note/264946576/)<br>
[Jekyll - Syntax highlighting](http://truongtx.me/2012/12/28/jekyll-bootstrap-syntax-highlighting/)<br>

## ToDo List

#### Code Demo
{% highlight c %}
#include <stdio.h>
int main(int argc, char **argv)
{
    printf("Hello, World!\n");
    return 0;
}
{% endhighlight %}

#### Math Formulation Demo
$$a^2 + b^2 = c^2$$

在default.html加上下面的代码即可
{% highlight html %}
<script type="text/javascript"
 src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
{% endhighlight %}

#### Jekyll常用命令
{% highlight bash %}
# 启动Jekyll
$ jekyll serve

# 创建第一篇博文
$ rake post title="Hello World"

# 根目录下创建页面
$ rake page name="about.md"

# 自定义目录下创建页面
$ rake page name="pages/about.md"

# 创建类似./pages/about/index.html目录结构的页面
$ rake page name="pages/about"

{% endhighlight %}

#### kramdown支持表格

表头      | 列1        | 列 2       |  列3        | 列4
----------|---------- -|:-----------|------------:|:--------------:
行1       | 内容       | 内容左对齐 | 内容右对齐  | 内容中间对齐
行2       | 内容       | 内容左对齐 | 内容右对齐  | 内容中间对齐
行3       | 内容       | 内容左对齐 | 内容右对齐  | 内容中间对齐
行4       | 内容       | 内容左对齐 | 内容右对齐  | 内容中间对齐

