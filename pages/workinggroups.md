---
title: The Broader Community 
layout: page
show_sidebar: false
hero_image: "../images/heros/pexels-jeffrey-eisen-1257101-31749011.jpg"
permalink: /groups/
---

A list of working groups: 
 
{% for wg in site.data.projects %}
- [{{wg.long}}]({{wg.website}})

{% endfor %}
