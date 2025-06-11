---
layout: home
---

Welcome to my personal site! I'm a developer who loves building things and sharing what I learn.

## Featured Projects

Check out some of my recent projects:

<div class="project-grid">
{% assign featured_projects = site.projects | where: "featured", true | limit: 3 %}
{% for project in featured_projects %}
  <div class="project-card">
    <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
    <p>{{ project.description }}</p>
    {% if project.tech_stack %}
      <p class="tech-stack">
        {% for tech in project.tech_stack %}
          <span class="tech-tag">{{ tech }}</span>
        {% endfor %}
      </p>
    {% endif %}
  </div>
{% endfor %}
</div>

<p><a href="/projects/" class="btn">View All Projects →</a></p>

## Latest Blog Posts

Here are my most recent thoughts and tutorials:

<!-- The home layout will automatically show recent posts below this content -->
