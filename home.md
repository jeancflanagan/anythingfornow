---
title: Home
permalink: "/"
layout: index
---

<h1 class="index-title">{{ site.title }}</h1>

{% for post in site.posts %}
  <article class="item">{{ post.date | date_to_string }} – <a href="{{ post.url }}">{{ post.title }}</a></article>
{% endfor %}
