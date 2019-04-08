---
layout: default
title: Artículos
---

<div id="articles">
  <h1>Articles</h1>
  <ul class="posts noList">
    {% for post in site.posts %}
      <li>
      	<span class="date">{% assign m = post.date | date: "%-m" %}
        {{ post.date | date: "%-d de" }}
        {% case m %}
          {% when '1' %}Enero
          {% when '2' %}Febrero
          {% when '3' %}Marzp
          {% when '4' %}Abril
          {% when '5' %}Mayo
          {% when '6' %}Junio
          {% when '7' %}Julio
          {% when '8' %}Agosto
          {% when '9' %}Septiembre
          {% when '10' %}Octubre
          {% when '11' %}Noviembre
          {% when '12' %}Diciembre
        {% endcase %}
        {{ post.date | date: "de %Y" }}</span>
      	<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      	<p class="description">{% if post.description %}{{ post.description  | strip_html | strip_newlines | truncate: 120 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 120 }}{% endif %}</p>
      </li>
    {% endfor %}
  </ul>
</div>