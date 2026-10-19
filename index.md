---
layout: default
title: "Claire Mitchell"
description: "Writing samples and personal projects."
nav: "home"
permalink: /
wide: true
---
<div class="home-grid{% unless site.data.reading.size > 0 %} no-sidebar{% endunless %}">
  <section class="intro">
    <h1>Hi, I'm Claire Mitchell</h1>
    <p class="lede">
      I write documentation, test software, and work on accessibility.
    </p>

    <p>
      For the past two years I've owned test strategy and documentation at Epic Systems, on healthcare software built for a customer in Finland that integrates with Kanta, the country's national health data repository. Before that I was a research assistant in an applied neuroscience lab. Most of both jobs was writing things down carefully enough that other people could use them.
    </p>
    <p>
      This site is where I keep what I've made. There are writing examples, a few programming projects, and my personal photography.
    </p>
    <p>
      I'm looking for work in technical writing or digital content management. You can reach me at <a href="mailto:Jobs@clairejmitchell.com">Jobs@clairejmitchell.com</a>.
    </p>
  </section>

  <section class="recent-pubs">
    <h2>Recent Publications</h2>
    <ul class="entry-list">
    {% for post in site.posts limit: 3 %}
      <li>
        <h3 class="entry-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <div class="entry-meta">{% if post.date_label %}{{ post.date_label }}{% else %}{{ post.date | date: "%B %Y" }}{% endif %}</div>
        <p class="entry-desc">{{ post.description }}</p>
      </li>
    {% endfor %}
    </ul>
    <p><a href="{{ '/writing/' | relative_url }}">All writing &rarr;</a></p>
  </section>

  {% if site.data.reading.size > 0 %}
  <aside class="reading-sidebar">
    <h2>What I'm Reading</h2>
    <ul class="reading-list">
    {% for item in site.data.reading %}
      <li>
        <a href="{{ item.url }}" target="_blank" rel="noopener">{{ item.title }}</a>
        {% if item.source %}<span class="reading-source">{{ item.source }}</span>{% endif %}
        {% if item.note %}<p class="reading-note">{{ item.note }}</p>{% endif %}
      </li>
    {% endfor %}
    </ul>
  </aside>
  {% endif %}
</div>
