---
layout: default
title: ""
---

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
  </li>
{% endfor %}
</ul>

{% if site.posts.size == 0 %}
Nothing here yet.
{% endif %}
