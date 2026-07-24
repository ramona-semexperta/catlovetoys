---
layout: default
title: Blog
permalink: /blog/
---

# The Blog

<div class="post-list-full">
{% for post in site.posts %}
  <div class="post-list-item">
    <p class="post-category">{{ post.categories | join: ", " | replace: "-", " & " }}</p>
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-date">{{ post.date | date: "%B %-d, %Y" }}</p>
    <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
  </div>
{% endfor %}
</div>
