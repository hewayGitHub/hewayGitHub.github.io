---
layout: page
title: Home
tagline: Supporting tagline
---
{% include JB/setup %}

### Who am I?

Name : 何威(Heway)  
Email : <heway.cn@gmail.com>  
Github : <https://github.com/hewayGitHub>  
Weibo : <http://weibo.com/heway1990/> 

A happy data worker!

### Hope U feel interested in

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


### Thanks

This theme is from [jekyll-bootstrap](http://jekyllbootstrap.com/)!



