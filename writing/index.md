---
layout: default
title: Writing archive
---
<div class="page-content wc-container">
  <h1>Writing</h1>  
  {% for post in site.categories.writing %}
  	{% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
  	{% if currentyear != year %}
    	{% unless forloop.first %}</ul>{% endunless %}
    		<h5>{{ currentyear }}</h5>
    		<ul class="posts">
    		{% capture year %}{{currentyear}}{% endcapture %} 
  		{% endif %}
    <li><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
{% endfor %}
<br>
<br>
<div class="post-footer">
    <div class="column-full">More stuff and updates in Juana’s personal blog: <a href="http://thejuanabanana.tumblr.com/">thejuanabanana.tumblr.com</a></div>
</div>