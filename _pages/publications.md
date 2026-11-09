---
layout: page
permalink: /publications/
title: Publications
description:
nav: true
nav_order: 2
_styles: >
  .pub { margin-bottom: 1.4rem; }
  .pub-title { font-weight: bold; }
  .post-header { display: none; }
  .pub-venue { color: var(--global-text-color-light); font-style: italic; }
  .pub-links a { margin-right: 0.4rem; font-size: 0.9rem; }
---

{% assign sections = "published:Publications|review:Under Review" | split: "|" %}

{% for sec in sections %}
{% assign parts = sec | split: ":" %}
{% assign papers = site.data.publications | where: "status", parts[0] %}
{% if papers.size > 0 %}

## {{ parts[1] }}

{% for p in papers %}

<div class="pub">
  <div class="pub-title">{{ p.title }}</div>
  <div class="pub-authors">{{ p.authors }}</div>
  <div class="pub-venue">{{ p.venue }}</div>
  {% if p.status == "published" %}
  <div class="pub-links">{% if p.paper %}<a href="{{ p.paper }}">[paper]</a>{% endif %}{% if p.code %}<a href="{{ p.code }}">[code]</a>{% endif %}{% if p.demo %}<a href="{{ p.demo }}">[demo]</a>{% endif %}</div>
  {% endif %}
</div>
{% endfor %}
{% endif %}
{% endfor %}
