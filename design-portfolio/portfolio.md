---
layout: page
title: 作品集
permalink: /portfolio/
---

# 设计作品集

## 按类别浏览

### 品牌设计
{% assign branding = site.portfolio | where: 'category', '品牌设计' %}
<div class="portfolio-grid">
  {% for item in branding %}
    <div class="portfolio-item">
      <a href="{{ item.url }}">
        <img src="{{ item.thumbnail }}" alt="{{ item.title }}" class="portfolio-thumbnail">
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
      </a>
    </div>
  {% endfor %}
</div>

### UI设计
{% assign ui_design = site.portfolio | where: 'category', 'UI设计' %}
<div class="portfolio-grid">
  {% for item in ui_design %}
    <div class="portfolio-item">
      <a href="{{ item.url }}">
        <img src="{{ item.thumbnail }}" alt="{{ item.title }}" class="portfolio-thumbnail">
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
      </a>
    </div>
  {% endfor %}
</div>

### 插画
{% assign illustration = site.portfolio | where: 'category', '插画' %}
<div class="portfolio-grid">
  {% for item in illustration %}
    <div class="portfolio-item">
      <a href="{{ item.url }}">
        <img src="{{ item.thumbnail }}" alt="{{ item.title }}" class="portfolio-thumbnail">
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
      </a>
    </div>
  {% endfor %}
</div>

<style>
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;
}
.portfolio-item {
  border: 1px solid #eee;
  border-radius: 8px;
  overflow: hidden;
  transition: transform 0.3s ease;
}
.portfolio-item:hover {
  transform: translateY(-5px);
}
.portfolio-thumbnail {
  width: 100%;
  height: 200px;
  object-fit: cover;
}
.portfolio-item h3 {
  padding: 1rem;
  margin: 0;
  font-size: 1.2rem;
}
.portfolio-item p {
  padding: 0 1rem 1rem;
  margin: 0;
  color: #666;
}
</style>