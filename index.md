---
layout: default
title: Home
description: Cybersecurity projects, tech experiments and things I have learned along the way.
---
<section class="hero">
  <div class="shell hero-grid">
    <div class="hero-copy">
      <p class="eyebrow">Cyber, tech &amp; whatever I'm building</p>
      <h1>Things I'm building,<br><span>breaking &amp; learning.</span></h1>
      <p class="hero-lede">This is my corner of the internet for cyber projects, technical experiments and notes that might be useful—or just interesting—to someone else.</p>
      <div class="hero-actions">
        <a class="button button-primary" href="{{ '/blog/' | relative_url }}">Read the blog</a>
        <a class="button button-secondary" href="{{ '/projects/' | relative_url }}">Explore projects</a>
      </div>
    </div>
    <div class="hero-mark" aria-hidden="true">
      <img src="{{ '/images/KelvSec.png' | relative_url }}" alt="" width="420" height="420">
    </div>
  </div>
</section>

<section class="shell section">
  <div class="section-heading">
    <div><p class="eyebrow">Recently posted</p><h2>From the blog</h2></div>
    <a class="text-link" href="{{ '/blog/' | relative_url }}">View all posts →</a>
  </div>
  <div class="card-grid">
    {% for post in site.posts limit: 3 %}
      <article class="card">
        <p class="card-meta"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%-d %b %Y' }}</time>{% if post.categories.size > 0 %} · {{ post.categories | first }}{% endif %}</p>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p>{{ post.description | default: post.excerpt | strip_html | truncate: 150 }}</p>
        <a class="card-link" href="{{ post.url | relative_url }}" aria-label="Read {{ post.title }}">Read article →</a>
      </article>
    {% endfor %}
  </div>
</section>

<section class="shell section projects-callout">
  <div>
    <p class="eyebrow">Projects &amp; experiments</p>
    <h2>Things I've been working on.</h2>
    <p>Finished builds, work in progress and technical rabbit holes—with enough detail for you to try them, learn from them or take them further.</p>
  </div>
  <a class="button button-secondary" href="{{ '/projects/' | relative_url }}">Browse projects</a>
</section>
