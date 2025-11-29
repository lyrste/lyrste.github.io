---
title: Home
layout: default
---

# Notes

This is the home

---

{% assign pages_list = site.pages | sort: "path" %}

<ul>
{% for p in pages_list %}
  {%- if p.url != "/" and p.layout == "default" and p.title -%}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
    </li>
  {%- endif -%}
{% endfor %}
</ul>
