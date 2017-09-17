---
layout:     post
title:      "Jekyll - additional study"
subtitle:   "advanced features and extension"
date:       2017-09-10
author:     "Daohui Li"
header-img: "img/study.jpg"
---

* TOC
{: toc}

The basic setup of a jekyll project can be seen in [my first post]({{ site.baseurl }}{% post_url 2017-09-07-hello-world %}). 

# Jekyll's how-to

* How to adding links to other posts:
{% raw %}
~~~ text
{{ site.baseurl }}{% post_url 2010-07-21-name-of-post %}
~~~
{% endraw %}

* How to include a file 

{% raw %}
~~~ text
{% include_relative directory/filename %}

For example,
{% include_relative assets/hello.txt %} 
~~~
{% endraw %}

{% include_relative assets/hello.txt %} 

# [kramdown syntax and features](https://kramdown.gettalong.org/syntax.html)

Jekyll uses *kramdown* to process markdown files (as seen in the markdown attribute in _config.yml). It is therefore beneficial to know the features of kramdown. The following are features I used:

* Enable math block in kramdown
---------------

*kramdown* uses '$$' to mark the math boundary. For example: 
<pre>$$ a^2 + b^2 = c^2 $$</pre> leads to $$ a^2 + b^2 = c^2 $$.

*Note*, one must add the following in the post to make the math block visible:
~~~ html
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
~~~

# Re-arrange file structure

*Motivation*: 
1. Cleanup the top-level directory so that it is not cluttered, 
2. in preparation of integrating with other technologies

*Steps*:
1. create _src_ directory and move all the source code, except _config.yml_, _.gitignore_, _Gemfile_, _package.json_, to _src_
2. add the following entry in _config.yml_:
~~~ text
  source: src
~~~

# Add Google Charts

1. Include google API and our own javascript, to be introduced next, in a html file
~~~ html

~~~

<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>      
      <script type="text/javascript" src="/assets/javascripts/draw-charts.js" charset="utf-8">
</script>   
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
