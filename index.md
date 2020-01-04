---
layout: default
---
## Purpose
## Setting up development environment

## Pinned documents

<div class="tiles">
{% assign sorted_pages = site.pages | sort: "title" %}
{% for page in sorted_pages %}
  {% if page.pinned == true %}
  <div class="tile">
  <a href="{% if site.baseurl == "/" %}{{ page.url }}{% else %}{{ page.url | prepend: site.baseurl}}{% endif %}">{{ page.title }}</a>
  {{ page.description | markdownify }}
  </div>
  {% endif %}
{% endfor %}
</div>

