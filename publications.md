---
layout: page
title: Les publications
---
Depuis l'annonce du projet éolien à Acigné, avec l'association [Courants Alternatifs](https://www.courantsalternatifs.com), nous nous sommes intéressés à l'impact de l'éolien. Nous avons notamment tenté de déméler le vrai du faux concernant les critiques qui lui sont fait. Ci-dessous, les articles publiés sur le [Blog de Courants Alternatifs](https://ca-acigne.blogspot.com/search/label/%C3%A9nergies)
<hr>
{% assign sorted = site.publications | reverse  %}
{% for publication in sorted %}
  <article>
    <h4>
      <a href="{{ publication.url | relative_url }}">
        {{ publication.title }}
      </a>
    </h4>
    <time datetime="{{ publication.date | date: "%Y-%m-%d" }}">{{ publication.date | date: "%d-%m-%Y" }}</time>
    {{ publication.excerpt }}
  </article>
{% endfor %}
