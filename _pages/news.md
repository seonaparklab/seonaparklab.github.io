---
layout: archive
title: "News"
permalink: /news/
---

<style>

.news-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(min(220px, 100%), 1fr));
  gap: 15px;
  max-width: 1000px;
  margin: 0 auto;
}

.news-card {
  background: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  overflow: hidden;
  transition: transform 0.2s;
}

.news-card:hover {
  transform: translateY(-3px);
}

.news-card img {
  width: 100%;
  height: auto;
  display: block;
}

.news-card h3 {
  margin: 8px;
  font-size: 1em;
  line-height: 1.2em;
}

.news-card p {
  margin: 0 8px 8px;
  font-size: 0.8em;
  color: #777;
}
</style>

<div class="news-container">
  {% assign news_items = site.data.news | sort: "sort_date" | reverse %}
  {% for news in news_items %}
  <div class="news-card">
    <a href="{{ news.url | relative_url }}">
      <img src="{{ news.image | relative_url }}" alt="{{ news.image_alt | default: news.title | escape }}" loading="lazy">
      <h3>{{ news.title }}</h3>
      <p><time datetime="{{ news.sort_date }}">{{ news.date }}</time></p>
    </a>
  </div>
  {% endfor %}
</div>
