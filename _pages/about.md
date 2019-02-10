---
layout: archive
title: "About"
permalink: /about/
header:
  image: "/images/header2.jpg"
author_profile: true
---

I'm a junior data scientist with a Masters Degree in Operations Research.
I started building my own Data Science Portfolio after graduating, currently
following https://www.youtube.com/watch?v=9rDhY1P3YLA&t=3s to step up my game!
---

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
