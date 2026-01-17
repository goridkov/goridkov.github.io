---
layout: single
title: "Projects"
permalink: /projects/
---

here's some cool projects I've worked on!

<div class="custom-project-gallery">
  {% assign my_projects = site.projects | reverse %}
  {% for project in my_projects %}
    <div class="project-item" style="margin-bottom: 50px; border-bottom: 1px solid #eee; padding-bottom: 40px;">
      
      {% if project.image %}
        <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" style="width: 100%; border-radius: 8px; margin-bottom: 20px;">
      {% endif %}

      <h2 style="margin-top: 0;">{{ project.title }}</h2>

      <div class="project-description">
        {{ project.content }}
      </div>
      
    </div>
  {% endfor %}
</div>
