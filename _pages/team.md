---
title: "IITH Compilers Team"
layout: gridlay
excerpt: "IITH Compilers Team members"
sitemap: false
permalink: /team/
---

# Team Members

 **We are  looking for new PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/openings) **.**


Jump to [Faculty](#faculty), [PhD Students](#phd-students), [Masters Students](#masters-students), [Alumni](#alumni).

## Faculty

<div class="row" style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin-bottom: 30px;">
{% for member in site.data.team_members %}
{% if member.type == 'faculty' %}
<div style="width: 280px; background: #fff; border: 1px solid #e0e0e0; border-radius: 10px; box-shadow: 0 2px 8px rgba(0,0,0,0.08); padding: 24px 20px; text-align: center; display: flex; flex-direction: column; align-items: center;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}"
       style="width: 150px; height: 150px; object-fit: cover; border-radius: 50%; border: 3px solid #ddd; margin-bottom: 14px;" />
  <h4 style="margin: 0 0 6px 0;"><a href="{{ member.url }}" target="_blank">{{ member.name }}</a></h4>
  <p style="margin: 0 0 4px 0; font-size: 0.9em; color: #555;"><i>{{ member.info }}</i></p>
  <p style="margin: 0 0 12px 0; font-size: 0.85em; color: #777;">{{ member.email }}</p>
  <ul style="text-align: left; padding-left: 18px; margin: 0; font-size: 0.85em; color: #444;">
  {% if member.number_educ >= 1 %}<li>{{ member.education1 }}</li>{% endif %}
  {% if member.number_educ >= 2 %}<li>{{ member.education2 }}</li>{% endif %}
  {% if member.number_educ >= 3 %}<li>{{ member.education3 }}</li>{% endif %}
  {% if member.number_educ >= 4 %}<li>{{ member.education4 }}</li>{% endif %}
  {% if member.number_educ >= 5 %}<li>{{ member.education5 }}</li>{% endif %}
  </ul>
</div>
{% endif %}
{% endfor %}
</div>

<br/>
## PhD Students

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}
{% if member.type == 'phd' %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive float-left object-fit-cover custom-padding">
  {% if member.url.value == 1 %}
  <h4><a href="{{ member.url.link }}" target="_blank">{{ member.name }}</a></h4>
  
  <p class="right">
  <i>{{ member.info }}<br>{{ member.email }}<br><b>Research Interests:</b> {{ member.interests }}</i>
  </p>
  {% endif %}

  {% if member.url.value == 0 %}
  <h4>{{ member.name }}</h4>
  <p class="right">
  <i>{{ member.info }}<br>{{ member.email }}<br><b>Research Interests:</b> {{ member.interests }}</i>
  </p>
  {% endif %}
  
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}

{% endfor %}
{% if  number_printed !=0  %}
{% if  even_odd ==0  %}
</div>
{% endif %}
{% endif %}

<br/>

## Masters Students
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}
{% if member.type == 'mtech' %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive float-left object-fit-cover custom-padding">
  {% if member.url.value == 1 %}
  <h4><a href="{{ member.url.link }}" target="_blank">{{ member.name }}</a></h4>
  <p class="right">
  <i>{{ member.info }}<br>{{ member.email }}<br><b>Research Interests:</b> {{ member.interests }}</i>
  </p>
  {% endif %}

  {% if member.url.value == 0 %}
  <h4>{{ member.name }}</h4>
  <p class="right">
  <i>{{ member.info }}<br>{{ member.email }}<br><b>Research Interests:</b> {{ member.interests }}</i>
  </p>
  {% endif %}

</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}

{% endfor %}

{% if  number_printed !=0  %}
{% if  even_odd ==0  %}
</div>
{% endif %}
{% endif %}

<br>

## Alumni
### Doctoral Students
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
  <p class="right">
  <i>{{ member.info }}</i>
  {% if member.thesis_link %}
  Thesis: <a href="{{ member.thesis_link }}" target="_blank">{{ member.thesis }}</a>
  {% elsif member.thesis != "NA" %}
  Thesis: {{ member.thesis }}
  {% endif %}
  <i>Next: {{ member.next }}</i>
  </p>
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


### Masters Students
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
  <p class="right">
  <i>{{ member.info }}</i>
  {% if member.thesis_link %}
  Thesis: <a href="{{ member.thesis_link }}" target="_blank">{{ member.thesis }}</a>
   {% elsif member.thesis != "NA" %}
  Thesis: {{ member.thesis }}
  {% endif %}
  <i>Next: {{ member.next }}</i>
  </p>
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