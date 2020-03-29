---
title: "Florentin Rochet - Home"
layout: homelay
excerpt: ""
sitemap: false
permalink: /
---


Intro: TODO

# Research Projects

{% assign number_printed = 0 %}
{% for project in site.data.projects %}

{% assign even_odd = number_printed | modulo: 2 %}

<!--{% if even_odd == 0 %}-->
<div class="row">
<!--{% endif %}-->

<div class="col-sm-12 clearfix">
 <div class="well">
  <pubtit>{{ project.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/projectpic/{{ project.image }}" class="img-responsive" width="25%" style="float: left" />
  <p>{{ project.description }}</p>
  <p> Linked publications: </p>
{% for publi in site.data.publist %}
{%if publi.id_project == project.projectid %}
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
{% endif %}
{% endfor %}
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
<!--{% if even_odd == 1 %}-->
</div>
<!--{% endif %}-->

<p> &nbsp; </p>




