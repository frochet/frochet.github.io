---
title: "Florentin Rochet - Home"
layout: homelay
excerpt: ""
sitemap: false
permalink: /
---

## Research Projects

{% assign number_printed = 0 %}
{% for project in site.data.projects %}

{% assign even_odd = number_printed | modulo: 2 %}


<div class="col-sm-12 clearfix">
 <div class="well">
  <projtit>{{ project.title }}</projtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/projectpic/{{ project.image }}" class="img-responsive" width="25%" style="float: left" />
  <p>{{ project.description }}</p>
  <p><b> Linked publications:</b> </p>
  <ul>
  {% if project.status == 1 %}
    <li> Upcoming publication! Stay tuned :-)</li>
  {% endif %}
  {% for publi in site.data.publist %}
  {% if publi.id_project == project.projectid %}
    <li>
    <p>{{ publi.title }}, 
  <strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
    </li>
{% endif %}
{% endfor %}
  </ul>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}

<p> &nbsp; </p>




