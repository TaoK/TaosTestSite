---
title: About
permalink: /about/
layout: single
---

This is **not** the base Jekyll theme. It's actually the minimal-mistakes theme, copied right into the project. Apparently they support that.

The instructions I followed are here: [Minimal Mistakes Quickstart Guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)

I've had a hard time understanding how page URLs end up working for Pages, so here's a test:

{% for cat in site.category-list %}
### {{ cat }}
<ul>
  {% for page in site.pages %}
    {% if page.resource == true %}
      {% for pc in page.categories %}
        {% if pc == cat %}
          <li><a href="{{ page.url }}">{{ page.title }}</a></li>
        {% endif %}   <!-- cat-match-p -->
      {% endfor %}  <!-- page-category -->
    {% endif %}   <!-- resource-p -->
  {% endfor %}  <!-- page -->
</ul>
{% endfor %}  <!-- cat -->