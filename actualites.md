---
layout: page
title: Actualités
---

{% for post in site.posts %}
  <article>
    <h4>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h4>
    <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date: "%d-%m-%Y" }}</time>
    {{ post.excerpt }}
  </article>
{% endfor %}
