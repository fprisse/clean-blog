---
layout: default
title: Logboek
---

<div class="post-cards-container">
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
  .post-cards-container {
    max-width: 100%;
    margin: 0 auto;
    padding: 0;
  }

  .post-card {
    background-color: white;
    padding: 2rem;
    margin-bottom: 2rem;
    border-radius: 6px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.1);
    width: 100%;
  }

  .post-date {
    color: #777;
    font-size: 0.9em;
    margin-top: -0.5rem;
    margin-bottom: 1rem;
  }
</style>
