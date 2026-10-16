---
layout: archive
title: "Members"
permalink: /members/
author_profile: true
---

<div class="members-container">
  {% for member in site.data.members %}
  <article class="member-card" aria-labelledby="member-{{ forloop.index }}">
    <div class="member-left">
      <p class="member-role">{{ member.role_detail | default: member.role | escape }}</p>
      <h2 id="member-{{ forloop.index }}">{{ member.name | escape }}</h2>
      {% if member.photo %}
      <img src="{{ member.photo | relative_url }}" alt="{{ member.name | escape }}" width="160" height="160" loading="lazy"{% if member.photo_position %} style="object-position: {{ member.photo_position | escape }};"{% endif %}>
      {% endif %}
      {% if member.research_interests %}
      <h3>Research Interests</h3>
      <ul>
        {% for item in member.research_interests %}
        <li>{{ item | escape }}</li>
        {% endfor %}
      </ul>
      {% endif %}
    </div>
    <div class="member-right">
      {% for section in site.data.member_sections %}
        {% assign entries = member[section.field] %}
        {% if entries %}
        <section>
          <h3>{{ member.section_titles[section.field] | default: section.title | escape }}</h3>
          {% if section.prose %}
          <p>{{ entries | escape }}</p>
          {% else %}
          <ul>
            {% for item in entries %}
            <li>{{ item | escape }}</li>
            {% endfor %}
          </ul>
          {% endif %}
        </section>
        {% endif %}
      {% endfor %}
      {% if member.contact %}
      <section>
        <h3>Contact</h3>
        <ul>
          {% for email in member.contact %}
          <li><a href="mailto:{{ email | escape }}">{{ email | escape }}</a></li>
          {% endfor %}
        </ul>
      </section>
      {% endif %}
    </div>
  </article>
  {% endfor %}
</div>

## Alumni

- Fan LI (Sep.2024 – Aug. 2025), MSc from National University of Singapore, and pre Senior Consultant at PwC. Research fields: ESG and Sustainability
