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

{% for post in site.posts %}
    <img src={{ post.header.overlay_image }} alt="Oops, there was an image here">
    <a href="{{ post.url }}">{{ post.title }}</a>
    {{ post.excerpt }}
{% endfor %}
