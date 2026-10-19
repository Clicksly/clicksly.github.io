---
layout: default
title: "Projects"
description: "Personal projects."
nav: "projects"
permalink: /projects/
redirect_from: /projects.html
---
<h1>Projects</h1>
<p class="lede">Things I've built, with notes on how and why.</p>

<ul class="entry-list">
{% assign items = site.projects | sort: "date" | reverse %}
{% for item in items %}
  <li>
    <h2 class="entry-title"><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h2>
    <div class="entry-meta">{% if item.date_label %}{{ item.date_label }}{% else %}{{ item.date | date: "%B %Y" }}{% endif %}</div>
    <p class="entry-desc">{{ item.description }}</p>
  </li>
{% endfor %}
</ul>
