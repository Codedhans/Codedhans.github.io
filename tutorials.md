---
layout: default
title: Tutorials
permalink: /tutorials/
---

<div class="page-header">
    <h1>Programming Tutorials</h1>
    <p>Step-by-step guides on the Art of Software—mastered on mobile.</p>
</div>

<div class="tutorial-grid">
    {% assign tutorials = site.posts | where: "category", "tutorial" %}
{% for post in tutorials %}
    {% endfor %}
    {% for post in tutorials %}
    <div class="tutorial-card">
        <div class="card-meta">
            <span class="tag">Tutorial</span>
            <span class="date">{{ post.date | date: "%b %d, %Y" }}</span>
        </div>
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        <a href="{{ post.url | relative_url }}" class="read-more-link">Start Learning →</a>
    </div>
    {% empty %}
    <div class="empty-state">
        <p>The lab is currently drafting new guides. Check back soon!</p>
    </div>
    {% endfor %}
</div>
