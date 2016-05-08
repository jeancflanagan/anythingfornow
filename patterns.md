---
title: Patterns
permalink: "/patterns/"
layout: post
---

{% for pattern in site.patterns %}
  <div class="pattern">
    <h1>{{ pattern.title }}</h1>
    {{ pattern.content | markdownify }}
    <textarea>{{ pattern.content }}</textarea>
    <textarea>{{ pattern.content | markdownify }}</textarea>
  </div>
{% endfor %}
