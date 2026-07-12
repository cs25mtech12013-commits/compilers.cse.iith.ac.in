---
title: "IITH Compilers Alumni"
layout: gridlay
excerpt: "IITH Compilers Alumni"
sitemap: false
permalink: /alumni/
---

# Alumni

Jump to [Doctoral Students](#doctoral-students), [Masters Students](#masters-students), [Undergrad Students](#undergrad-students).

## Doctoral Students
{% assign number_printed_phd = 0 %}
{% for member in site.data.alumni %}
{% if member.value == "phd" %}

{% assign even_odd_phd = number_printed_phd | modulo: 2 %}
{% if even_odd_phd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive float-left object-fit-cover custom-padding">
  <h4>{{ member.name }}</h4>
  <p class="right"><i>{{ member.info }}<br>{% if member.thesis_link %}Thesis: <a href="{{ member.thesis_link }}" target="_blank">{{ member.thesis }}</a><br>{% elsif member.thesis != "NA" %}Thesis: {{ member.thesis }}<br>{% endif %}Next: {{ member.next }}</i></p>
</div>

{% assign number_printed_phd = number_printed_phd | plus: 1 %}
{% if even_odd_phd == 1 %}
</div>
{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd_phd = number_printed_phd | modulo: 2 %}
{% if even_odd_phd == 1 %}
</div>
{% endif %}

<br/>

## Masters Students
{% assign number_printed_mtech = 0 %}
{% for member in site.data.alumni %}
{% if member.value == "mtech" %}

{% assign even_odd_mtech = number_printed_mtech | modulo: 2 %}
{% if even_odd_mtech == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive float-left object-fit-cover custom-padding">
  <h4>{{ member.name }}</h4>
  <p class="right"><i>{{ member.info }}<br>{% if member.thesis_link %}Thesis: <a href="{{ member.thesis_link }}" target="_blank">{{ member.thesis }}</a><br>{% elsif member.thesis != "NA" %}Thesis: {{ member.thesis }}<br>{% endif %}Next: {{ member.next }}</i></p>
</div>

{% assign number_printed_mtech = number_printed_mtech | plus: 1 %}
{% if even_odd_mtech == 1 %}
</div>
{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd_mtech = number_printed_mtech | modulo: 2 %}
{% if even_odd_mtech == 1 %}
</div>
{% endif %}

<br/>

## Undergrad Students
{% assign number_printed_btech = 0 %}
{% for member in site.data.alumni %}
{% if member.value == "btech" %}

{% assign even_odd_btech = number_printed_btech | modulo: 2 %}
{% if even_odd_btech == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive float-left object-fit-cover custom-padding">
  <h4>{{ member.name }}</h4>
  <p class="right"><i>{{ member.info }}<br>{% if member.thesis_link %}Thesis: <a href="{{ member.thesis_link }}" target="_blank">{{ member.thesis }}</a><br>{% elsif member.thesis != "NA" %}Thesis: {{ member.thesis }}<br>{% endif %}Next: {{ member.next }}</i></p>
</div>

{% assign number_printed_btech = number_printed_btech | plus: 1 %}
{% if even_odd_btech == 1 %}
</div>
{% endif %}
{% endif %}
{% endfor %}

{% assign even_odd_btech = number_printed_btech | modulo: 2 %}
{% if even_odd_btech == 1 %}
</div>
{% endif %}

<br/>
