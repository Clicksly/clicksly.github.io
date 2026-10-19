---
layout: default
title: "Photography"
description: "Photography."
nav: "photography"
permalink: /photography/
redirect_from: /photography.html
---
<h1>Photography</h1>
<p class="lede">Original photography. Shot on Canon, graded in Lightroom. Not for Sale.</p>

<ul class="entry-list">
{% assign items = site.photography | sort: "date" | reverse %}
{% for item in items %}
  <li>
    <h2 class="entry-title"><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h2>
    <div class="entry-meta">{% if item.date_label %}{{ item.date_label }}{% else %}{{ item.date | date: "%B %Y" }}{% endif %}</div>
    <p class="entry-desc">{{ item.description }}</p>
  </li>
{% endfor %}
</ul>
