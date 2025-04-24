---
layout: default
title: Logboek
---

<div class="wrapper">

  {% for post in site.posts %}
    <div class="post-card">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p>{{ post.excerpt }}</p>
      <a href="{{ post.url }}">Read more →</a>
    </div>
  {% endfor %}
</div>

<style>
  .post-card {
    background-color: white;
    padding: 2rem;
    margin-bottom: 2rem;
    border-radius: 6px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.1);
  }

  .post-date {
    color: #777;
    font-size: 0.9em;
    margin-top: -0.5rem;
    margin-bottom: 1rem;
  }

  .wrapper {
    max-width: 740px;
    margin: 0 auto;
    padding: 2rem;
  }
</style>
