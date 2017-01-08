---
layout: default
title: Banana Fish archive
---
<div class="page-content wc-container">
  <h4>Banana Fish is a handcrafted leather shoes project. Inspired in the model of school shoes in Buenos Aires, but for people all ages, gender or style. The brand also creates other garments related to youth and storytelling.</h4>  
  <br>
  <br>
  {% for post in site.categories.banana %}
  	{% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
  	{% if currentyear != year %}
    	{% unless forloop.first %}</ul>{% endunless %}
    		<h5>{{ currentyear }}</h5>
    		<ul class="posts">
    		{% capture year %}{{currentyear}}{% endcapture %} 
  		{% endif %}
    <li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
  {% endfor %}