---
title: "CIBM Lab - Publications"
layout: gridlay
excerpt: "CIBM Lab -- Publications"
sitemap: false
permalink: /publications/
---


# Publications

{% for publi in site.data.publist %}

  {&#x2022; { publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
