---
title: "Spring Boot Security"
layout: archive
permalink: categories/security
author_profile: true
types: posts
---

- 인프런 정수원의 Security를 듣고 정리한 글 입니다.

- Spring boot 2.7 이전 버전입니다 (WebSecurityConfigurerAdapter deprecated 되기 전)

{% assign posts = site.categories['security']%}
{% for post in posts %} 
  {% include archive-single.html type=page.entries_layout %} 
{% endfor %}