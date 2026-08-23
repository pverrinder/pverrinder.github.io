---
layout: default
title: Writing
---

# Writing

My attempts at writing. Currently empty because I haven't attempted anything yet.

{% assign items = site.writing | where_exp: "i", "i.name != 'index.md'" %}
<ul>
{% for item in items %}
  <li><a href="{{ item.url | relative_url }}">{{ item.title }}</a>{% if item.summary %} — {{ item.summary }}{% endif %}</li>
{% endfor %}
{% if items.size == 0 %}
  <li><em>Coming soon</em></li>
{% endif %}
</ul>
