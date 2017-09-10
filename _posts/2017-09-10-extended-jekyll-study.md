---
layout:     post
title:      "Jekyll - additional study"
subtitle:   "advanced features and extension"
date:       2017-09-10
author:     "Daohui Li"
header-img: "img/study.jpg"
---

The basic setup of a jekyll project can be seen in [my first post]({{ site.baseurl }}{% post_url 2017-09-07-hello-world %}). I am listing a few features I encounted:

* TOC
{: toc}


# Jekyll's advanced features

* Add link to other posts:
{% raw %}
<pre>{{ site.baseurl }}{% post_url 2010-07-21-name-of-post %}</pre>
{% endraw %}

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

# Integrating with _webpack_ and _react_


*TODO*.

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
