---
layout: archive
permalink: /portfolio/
title: "My Portfolio"
author_profile: true
classes: wide
excerpt: "Here you can find a showcase of my projects and my programming abilities"
header:
  overlay_image: "assets/images/projects.jpg"
  overlay_filter: 0.5

  caption: "Photo credit: [**Unsplash**](https://unsplash.com/photos/OqtafYT5kTw)"
---

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
