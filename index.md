---
layout: default
title: Blog
paginate: true
---


<div class="wrapper">
  <h1>Blog</h1>

  {% for post in paginator.posts %}
    <div class="post-card">
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
      <a href="{{ site.baseurl }}{{ post.url }}">Read more →</a>
    </div>
  {% endfor %}

  <div class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ site.baseurl }}{{ paginator.previous_page_path }}">← Newer Posts</a>
    {% endif %}
    {% if paginator.next_page %}
      <a href="{{ site.baseurl }}{{ paginator.next_page_path }}">Older Posts →</a>
    {% endif %}
  </div>
</div>
