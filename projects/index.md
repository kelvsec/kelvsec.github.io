---
layout: default
title: Projects
description: Cybersecurity and technology projects I have built, explored and learned from.
permalink: /projects/
---
<section class="shell page-intro">
  <p class="eyebrow">Projects</p>
  <h1>Things I've built and explored.</h1>
  <p>A mix of finished projects, experiments and ideas I'm still tinkering with. If something here helps with your own project, even better.</p>
</section>
<section class="shell section section-flush">
  <div class="card-grid">
    {% assign projects = site.projects | sort: 'date' | reverse %}
    {% for project in projects %}
      <article class="card">
        <p class="card-meta"><time datetime="{{ project.date | date_to_xmlschema }}">{{ project.date | date: '%-d %b %Y' }}</time>{% if project.status %} · {{ project.status }}{% endif %}</p>
        <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
        <p>{{ project.description | default: project.excerpt | strip_html }}</p>
        <a class="card-link" href="{{ project.url | relative_url }}" aria-label="View {{ project.title }}">View project →</a>
      </article>
    {% endfor %}
  </div>
</section>
