---
layout: default
title: Tutorials
permalink: /tutorials/
---

<div class="page-header">
    <h1>Programming Tutorials</h1>
    <p>Step-by-step guides on the Art of Software.</p>
</div>

<div class="tutorial-grid">
    {% for post in site.posts %}
        {% if post.category == "tutorial" %}
        <div class="tutorial-card">
            <div class="card-meta">
                <span class="tag">Tutorial</span>
                <span class="date">{{ post.date | date: "%b %d, %Y" }}</span>
            </div>
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
            <p>{{ post.excerpt | strip_html | truncatewords: 15 }}</p>
            <a href="{{ post.url | relative_url }}" class="read-more-link">Start Learning →</a>
        </div>
        {% endif %}
    {% endfor %}
</div>

<div style="text-align: center; margin-top: 40px; color: #666;">
    <p>New mobile-dev guides are currently being drafted in the lab.</p>
</div>
