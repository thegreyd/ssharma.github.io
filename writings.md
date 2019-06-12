---
layout: page
title: Writings
permalink: /writings/
---

<ul class="posts">

  {% for post in site.posts %}
    {% if post.title == "A normal day in the life of a speedster" or post.title == "Mystery: A Father Daughter adventure" or post.title == "The Ballad of Valentine" %}
        <li><span>{{ post.date | date_to_string }}</span> » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>