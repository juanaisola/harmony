---
layout: default
title: Writing archive
---
<div class="page-content wc-container">
  <h1>Writing</h1>
  <div class="posts">
    {% for post in site.categories.writing %}
    <div class="post">
      <h3 class="post-title">
        <a href="{{ post.url | prepend: site.baseurl | prepend: site.url }}">
          {{ post.title }}
        </a>
      </h3>

      <p class="post-meta">
        {% if (post.categories.size > 0 %}
        <span class="categories">
        {{ post.categories | array_to_sentence_string }}
        </span> |
        {% endif %}
        <span class="post-date">
        {{ post.date | date: "%b, %Y" }} 
        </span>
      </p>          
                
      <p>
        {{ post.excerpt }}  
      </p>
      <p>
        <a href="{{ post.url | prepend: site.baseurl | prepend: site.url }}" title="{{ post.title}}">
          Read More
      </a>
      </p>
    </div>
    {% endfor %}
  </div>
  <br>
  <br>
  <div class="post-footer">
      <div class="column-full">More stuff and updates in Juana’s personal blog: <a href="http://thejuanabanana.tumblr.com/">thejuanabanana.tumblr.com</a></div>
  </div>
</div>