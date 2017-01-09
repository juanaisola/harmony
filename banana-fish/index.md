---
layout: default
title: Banana Fish archive
---
<div class="page-content wc-container">
  <img align="right" src="{{ site.url }}/assets/images/banana-fish.jpg" style="float: right; height: 400px; margin: 5px;">
  <h4><b><a href="http://www.bananafishzapatos.com/">Banana Fish</a></b> is a handcrafted leather shoes project founded by Juana Isola in 2014. Inspired in the model of school shoes in Buenos Aires, but for people all ages, gender or style. The brand also creates other garments related to youth and storytelling.</h4>
  <br>
  <br>
  {% for post in site.categories.banana-fish %}
    {% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
    {% if currentyear != year %}
      {% unless forloop.first %}</ul>{% endunless %}
        <h5>{{ currentyear }}</h5>
        <ul class="posts">
        {% capture year %}{{currentyear}}{% endcapture %} 
      {% endif %}
    <li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
  {% endfor %}