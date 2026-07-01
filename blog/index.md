---
layout: default
title: Blog
description: Notes, ideas and useful things I have picked up while working with cybersecurity and technology.
permalink: /blog/
---
<section class="shell page-intro">
  <p class="eyebrow">Blog</p>
  <h1>Notes, ideas and useful bits.</h1>
  <p>Write-ups from things I've tried, learned or found interesting while working with cyber and tech.</p>
</section>
<section class="shell section section-flush">
  <div class="article-list">
    {% for post in site.posts %}
      <article class="list-item">
        <div class="list-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%-d %b %Y' }}</time></div>
        <div>
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p>{{ post.description | default: post.excerpt | strip_html }}</p>
          {% if post.tags.size > 0 %}<p class="mini-tags">{{ post.tags | join: ' · ' }}</p>{% endif %}
        </div>
      </article>
    {% endfor %}
  </div>
</section>
