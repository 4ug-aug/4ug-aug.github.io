---
layout: page
title: Projects
permalink: /projects/
---

Here are some projects I've built or am currently working on:

{% for project in site.projects %}
  <div class="project-card">
    <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
    <p>{{ project.description }}</p>
    {% if project.tech_stack %}
      <p><strong>Tech:</strong> {{ project.tech_stack | join: ", " }}</p>
    {% endif %}
  </div>
{% endfor %}
