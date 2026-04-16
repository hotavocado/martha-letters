---
layout: default
title: Martha
---
<div class="index-header">
  <h1>Session newsletters</h1>
</div>

<ul class="newsletter-list">
  {% assign newsletters = site.quotes | sort: 'date' | reverse %}
  {% for newsletter in newsletters %}
  <li>
    <a href="{{ newsletter.url | relative_url }}">
      <span class="list-title">{{ newsletter.title }}</span>
      <span class="list-date">{{ newsletter.date | date: "%B %-d, %Y" }}</span>
    </a>
  </li>
  {% endfor %}
</ul>
