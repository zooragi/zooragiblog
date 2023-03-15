---
title: "Docker"
layout: archive
permalink: categories/docker
author_profile: true
types: posts
---

Docker

{% assign posts = site.categories['docker']%}
{% for post in posts %} 
  {% include archive-single.html type=page.entries_layout %} 
{% endfor %}