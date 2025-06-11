---
layout: page
title: Projects
permalink: /projects/
---

<div class="page-header">
  <h1>🚀 My Projects</h1>
  <p class="page-description">A collection of things I've built, learned from, and am proud to share</p>
</div>

<div class="projects-grid">
{% for project in site.projects %}
  <article class="project-card">
    {% if project.thumbnail %}
    <div class="project-thumbnail">
      <a href="{{ project.url }}">
        <img src="{{ project.thumbnail }}" alt="{{ project.thumbnail_alt | default: project.title }}" loading="lazy">
      </a>
      {% if project.status %}
      <span class="project-status status-{{ project.status }}">{{ project.status | capitalize }}</span>
      {% endif %}
    </div>
    {% endif %}
    
    <div class="project-content">
      <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
      <p class="project-description">{{ project.description }}</p>
      
      {% if project.tech_stack %}
      <div class="tech-stack">
        {% for tech in project.tech_stack limit:4 %}
        <span class="tech-tag">{{ tech }}</span>
        {% endfor %}
        {% if project.tech_stack.size > 4 %}
        <span class="tech-tag more">+{{ project.tech_stack.size | minus: 4 }} more</span>
        {% endif %}
      </div>
      {% endif %}
      
      <div class="project-footer">
        <time class="project-date">{{ project.date | date: "%B %Y" }}</time>
        <div class="project-links-mini">
          {% if project.demo_url %}
          <a href="{{ project.demo_url }}" class="link-demo" title="View Demo" target="_blank">🔗</a>
          {% endif %}
          {% if project.github_url %}
          <a href="{{ project.github_url }}" class="link-github" title="View Code" target="_blank">📁</a>
          {% endif %}
        </div>
      </div>
    </div>
  </article>
{% endfor %}
</div>

{% if site.projects.size == 0 %}
<div class="empty-state">
  <p>🛠️ Projects coming soon! I'm currently working on some exciting stuff.</p>
</div>
{% endif %}
