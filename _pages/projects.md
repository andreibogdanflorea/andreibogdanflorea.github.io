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


{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>

{% include paginator.html %}
