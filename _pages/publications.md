---
title: "Florentin Rochet - Publications"
layout: gridlay
excerpt: "Florentin Rochet -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

{% for publi in site.data.publist %}

  <b>{{ publi.title }} </b><br />
  <em>{{ publi.authors }} </em><br />
  In:<em> {{ publi.in }} </em><br />
  <a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

