---
layout: default
title: Wang Yu's Blog
---
{% include JB/setup %}
{% assign first_post = site.posts.first %}
<div id="post">
<h1> <a href = "{{ first_post.url }}">
{{ first_post.title }}
</a></h1>

<div class="authoring">
  <span>{{ first_post.date | date: "%B %e, %Y" }}</span>
</div>
{{ first_post.content }}
</div>

<div style="line-height:180%;">
  出处：<a href="{{ first_post.url }}">http://wangywy.github.com{{ first_post.url }}</a><br>
  声明：本文采用以下协议进行授权： <a href="http://creativecommons.org/licenses/by-nc-nd/3.0/deed.zh">自由转载-非商用-非衍生-保持署名|Creative Commons BY-NC-ND 3.0</a> ，转载请注明作者及出处。<br><br>
</div>

<h1> Newest 10 Posts </h1>
<ul class="posts">
  {% for post in site.posts limit:10 %}
  <li><span class="post_date">{{ post.date | date: "%B %e, %Y" }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
