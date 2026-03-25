---
layout: default
title: Blog
permalink: /blog/
---

<div class="page-header">
    <h1>Tech Insights & News</h1>
    <p>Staying ahead of the curve in the Art of Software.</p>
</div>

<div class="tutorial-grid">
    {% for post in site.posts %}
        {% if post.category != "tutorial" %}
        <div class="tutorial-card">
            <div class="card-meta">
                <span class="tag">News</span>
                <span class="date">{{ post.date | date: "%b %d, %Y" }}</span>
            </div>
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
            <p>{{ post.excerpt | strip_html | truncatewords: 15 }}</p>
            <a href="{{ post.url | relative_url }}" class="read-more-link">Read Article →</a>
        </div>
        {% endif %}
    {% endfor %}
</div>
