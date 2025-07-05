---
title: "Spring Boot Cloud"
layout: archive
permalink: categories/cloud
author_profile: true
types: posts
---

- spring boot cloud를 이용하여 MSA 서비스 구축


{% assign posts = site.categories['cloud']%}
{% for post in posts %} 
  {% include archive-single.html type=page.entries_layout %} 
{% endfor %}