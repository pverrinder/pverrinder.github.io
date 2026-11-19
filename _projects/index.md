---
layout: default
title: Projects
---

# Projects

Here are some of my projects. Please enjoy but don't like or comment becuase this isn't social media.

{% assign items = site.projects | where_exp: "i", "i.name != 'index.md'" %}
<ul>
{% for item in items %}
  <li><a href="{{ item.url | relative_url }}">{{ item.title }}</a>{% if item.summary %} — {{ item.summary }}{% endif %}</li>
{% endfor %}
{% if items.size == 0 %}
  <li><em>Coming soon</em></li>
{% endif %}
</ul>

<p class="corner-text">Nobody here but us potatoes.</p>
