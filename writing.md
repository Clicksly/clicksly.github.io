---
layout: default
title: "Writing"
description: "Writing samples."
nav: "writing"
permalink: /writing/
redirect_from: /writing.html
---
<h1>Writing</h1>
<p class="lede">Technical writing examples, articles, and works of fiction.</p>

<ul class="entry-list">
{% for post in site.posts %}
  <li>
    <h2 class="entry-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <div class="entry-meta">{% if post.date_label %}{{ post.date_label }}{% else %}{{ post.date | date: "%B %Y" }}{% endif %}</div>
    <p class="entry-desc">{{ post.description }}</p>
  </li>
{% endfor %}
</ul>
