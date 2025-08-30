---
layout: archive
title: "Members"
permalink: /members/
author_profile: true
redirect_from:
  - /resume
---
---

<style>
.members-container {
  display: flex;
  flex-direction: column;
  gap: 30px;
}

/* 每个成员卡片 */
.member-card {
  display: flex;
  flex-wrap: wrap; /* 手机小屏时换行 */
  background-color: #ffffff;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
  overflow: hidden;
  padding: 20px;
}

/* 左侧基础信息 */
.member-left {
  flex: 0 0 350px; /* 左侧固定宽度 */
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-right: 20px;
  border-right: 1px solid #eee;
  margin-bottom: 10px;
}

.member-left h4 {
  margin: 0 0 10px 0;
  text-align: center;
  font-weight: 600;
}

.member-left img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 15px;
}

.member-left strong {
  margin-top: 10px;
  text-align: center;
}

/* 右侧详细信息 */
.member-right {
  flex: 1;
  padding-left: 20px;
}

.member-right h4 {
  margin-top: 0;
  margin-bottom: 5px;
  font-weight: 600;
}

.member-right ul {
  margin: 0 0 15px 20px;
}

.member-right li {
  margin-bottom: 5px;
}

/* 响应式：小屏幕时左右堆叠 */
@media (max-width: 700px) {
  .member-card {
    flex-direction: column;
  }
  .member-left {
    border-right: none;
    border-bottom: 1px solid #eee;
    padding-right: 0;
    padding-bottom: 15px;
  }
  .member-right {
    padding-left: 0;
  }
}
</style>


<div class="members-container">
  {% for member in site.data.members %}
  <div class="member-card">
    <!-- 左侧：基本信息 -->
    <div class="member-left">
      <h2>{{ member.role }} </h2>
      <h2> ({{ member.name }})</h2>
      <img src="{{ member.photo }}" alt="{{ member.name }}">
      {% if member.research_interests %}
      <strong>Research Interests:</strong>
      <ul>
        {% for item in member.research_interests %}
        <li>{{ item }}</li>
        {% endfor %}
      </ul>
      {% endif %}
    </div>

    <!-- 右侧：详细信息 -->
    <div class="member-right">
      {% if member.education %}
      <h3>Education</h3>
      <ul>
        {% for item in member.education %}
        <li>{{ item }}</li>
        {% endfor %}
      </ul>
      {% endif %}

      {% if member.research_experience %}
      <h3>Work & Research Experience</h3>
      <ul>
        {% for item in member.research_experience %}
        <li>{{ item }}</li>
        {% endfor %}
      </ul>
      {% endif %}

      {% if member.awards %}
      <h3>Awards</h3>
      <ul>
        {% for item in member.awards %}
        <li>{{ item }}</li>
        {% endfor %}
      </ul>
      {% endif %}

      {% if member.contact %}
      <h3>Contact</h3>
      <ul>
        {% for item in member.contact %}
        <li>{{ item }}</li>
        {% endfor %}
      </ul>
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>

---

# Alumni

---

- Fan LI (Sep.2024 – Aug. 2025), MSc from National University of Singapore, and pre Senior Consultant at PwC. Research fields: ESG and Sustainability