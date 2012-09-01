---
layout: page
title: 欢迎来到“波”的世界!
tagline: 
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li>
      <div class="post-div box-shadow border-radius">
        <div class="post-div-header">
          <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
        </div>
        <div class="post-div-preview">
          {{ post.content | strip_html | truncate: 250 }}
        </div>
        <div class="post-div-index">
          <div class="day">{{ post.date | date: "%d" }}</div>
          <div class="month">{{ post.date | date: "%b" }}</div>
        </div>
        <div class="post-div-link"><a href="{{ BASE_PATH }}{{ post.url }}">查看原文 >></a></div>
      </div>
    </li>
  {% endfor %}
</ul>

