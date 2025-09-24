---
layout: category
title: Roots
category: roots
permalink: /roots
---
<h1>Roots</h1>
<ul>
  {% for post in site.posts %}
    {% if post.categories contains "roots" %}
      <li style="margin-bottom: 20px;">
        {% if post.image %}
          <a href="{{ post.url }}">
            <img src="{{ post.image }}" alt="{{ post.title }}" style="width:300px; height:auto; display:block;">
          </a>
        {% endif %}
        <a href="{{ post.url }}" style="font-size: 1.2em; font-weight: bold;">{{ post.title }}</a>
        <span>{{ post.date | date: "%d %b %Y" }}</span>
      </li>
    {% endif %}
  {% endfor %}
</ul>
