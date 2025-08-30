---
layout: archive
title: "News"
permalink: /news/
---

<style>
/* ====== 新闻卡片样式 ====== */
.news-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
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
  height: 120px;
  object-fit: cover;
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
  {% for news in site.data.news %}
  <div class="news-card">
    <a href="{{ news.url }}">
      <img src="{{ news.image }}" alt="{{ news.title }}">
      <h3>{{ news.title }}</h3>
      <p>{{ news.date }}</p>
    </a>
  </div>
  {% endfor %}
</div>
