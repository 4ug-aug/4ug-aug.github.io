---
layout: home
---

<div class="hero-section">
  <h1 class="hero-title">Welcome to my corner of the web</h1>
  <p class="hero-subtitle">I'm a developer who loves building things and sharing what I learn along the way.</p>
</div>

<section class="featured-section">
  <div class="section-header">
    <h2>🚀 Featured Projects</h2>
    <p class="section-description">Check out some of my recent work and experiments</p>
  </div>

  <div class="project-grid">
  {% assign featured_projects = site.projects | where: "featured", true | limit: 3 %}
  {% if featured_projects.size > 0 %}
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
  {% else %}
    <div class="empty-state">
      <p>🛠️ Projects coming soon! I'm currently working on some exciting stuff.</p>
    </div>
  {% endif %}
  </div>

  <div class="section-footer">
    <a href="/projects/" class="btn btn-primary">View All Projects →</a>
  </div>
</section>

<section class="blog-section">
  <div class="section-header">
    <h2>📝 Latest from the Blog</h2>
    <p class="section-description">Recent thoughts, tutorials, and lessons learned</p>
  </div>
  
  <!-- The home layout will automatically show recent posts below this content -->
</section>
