---
layout: page
title: "Projects"
permalink: /projects/
---

{% assign ordered_categories = "Research,University,Personal" | split: "," %}

{% for cat in ordered_categories %}
{% assign cat_projects = site.projects | where: "category", cat | sort: "date" | reverse %}
{% if cat_projects.size > 0 %}
<section class="projects-section">
  <h2 class="projects-section-title">{{ cat }}</h2>
  <div class="projects-grid">
    {% for project in cat_projects %}
    <div class="project-card">
      <div class="project-card-header">
        <h3 class="project-card-title"><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
        {% if project.context %}<span class="project-context-badge">{{ project.context }}</span>{% endif %}
      </div>
      <p class="project-card-date">{{ project.date | date: "%B %Y" }}</p>
      {% if project.description %}<p class="project-card-desc">{{ project.description }}</p>{% endif %}
      {% if project.technologies %}<p class="project-card-tech">{{ project.technologies | join: " · " }}</p>{% endif %}
      <a href="{{ project.url | relative_url }}" class="btn-see-more">See more →</a>
    </div>
    {% endfor %}
  </div>
</section>
{% endif %}
{% endfor %}
