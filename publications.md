---
layout: page
title: Les publications
---
Depuis l'annonce du projet éolien à Acigné, avec l'association [Courants Alternatifs](https://www.courantsalternatifs.com), nous nous sommes intéressés à l'impact de l'éolien. Nous avons notamment tenté de déméler le vrai du faux concernant les critiques qui lui sont fait.
<hr>
{% assign sorted = site.publications | reverse  %}
{% for publication in sorted %}
  <article>
    <div>
      <h4>
        <a href="{{ publication.url | relative_url }}">
        {{ publication.title }}
        </a>
      </h4>
      <time datetime="{{ publication.date | date: "%Y-%m-%d" }}">{{ publication.date | date: "%d-%m-%Y" }}</time>
      {% if publication.featured-image %}
      <br><img src="{{ publication.featured-image | relative_url }}" class="featured-image"/>
      {% endif %}
      {% if publication.cablogurl %}
        {{ publication.content }}
        Pour lire l'article sur le site de Courants Alternatifs, <a href="{{ publication.cablogurl }}">cliquez sur ce lien</a>.
      {% else %}
        {{ publication.excerpt }}
        <a href="{{ publication.url | relative_url }}">Lire la suite...</a>
      {% endif %}
    </div>
  </article>
{% endfor %}
