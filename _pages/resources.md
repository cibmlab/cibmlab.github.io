---
title: "CIBM Lab - Resources"
layout: gridlay
excerpt: "CIBM Lab -- Resources"
sitemap: false
permalink: /resources/
---


# Resources

{% assign number_printed = 0 %}
{% for resou in site.data.reslist %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <h4>{{ resou.title }}</h4>
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/{{ resou.image }}" class="img-responsive" /> <br> <!-- width="60%" style="float: left" /> -->
  {% if resou.number_link == 1 %}
  <li> <a href="{{ resou.link1.url }}">{{ resou.link1.display }}</a>
  <p>{{ resou.link1.description }}</p></li>
  {% endif %}
  {% if resou.number_link == 2 %}
  <ul>
  <li> <a href="{{ resou.link1.url }}">{{ resou.link1.display }}</a></li>
  <li> <a href="{{ resou.link2.url }}">{{ resou.link2.display }}</a></li> 
  </ul>
  {% endif %}
  {% if resou.number_link == 3 %}
  <li> <a href="{{ resou.link1.url }}">{{ resou.link1.display }}</a>
  <p>{{ resou.link1.description }}</p></li>
  <li> <a href="{{ resou.link2.url }}">{{ resou.link2.display }}</a>
  <p>{{ resou.link2.description }}</p></li>
  <li> <a href="{{ resou.link3.url }}">{{ resou.link3.display }}</a>
  <p>{{ resou.link3.description }}</p></li> 
  {% endif %}
  {% if resou.number_link == 4 %}
  <li> <a href="{{ resou.link1.url }}">{{ resou.link1.display }}</a>
  <p>{{ resou.link1.description }}</p></li>
  <li> <a href="{{ resou.link2.url }}">{{ resou.link2.display }}</a>
  <p>{{ resou.link2.description }}</p></li>
  <li> <a href="{{ resou.link3.url }}">{{ resou.link3.display }}</a>
  <p>{{ resou.link3.description }}</p></li>
  <li> <a href="{{ resou.link4.url }}">{{ resou.link4.display }}</a>
  <p>{{ resou.link4.description }}</p></li> 
  {% endif %}
  {% if resou.number_link == 5 %}
  <li> <a href="{{ resou.link1.url }}">{{ resou.link1.display }}</a>
  <p>{{ resou.link1.description }}</p></li>
  <li> <a href="{{ resou.link2.url }}">{{ resou.link2.display }}</a>
  <p>{{ resou.link2.description }}</p></li>
  <li> <a href="{{ resou.link3.url }}">{{ resou.link3.display }}</a>
  <p>{{ resou.link3.description }}</p></li>
  <li> <a href="{{ resou.link4.url }}">{{ resou.link4.display }}</a>
  <p>{{ resou.link4.description }}</p></li>
  <li> <a href="{{ resou.link5.url }}">{{ resou.link5.display }}</a>
  <p>{{ resou.link5.description }}</p></li> 
  {% endif %}
  </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>
