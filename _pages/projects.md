---
layout: page
permalink: /projects/
title: Projects
description:
nav: true
nav_order: 3
_styles: >
  .post-header { display: none; }
  .proj { margin-bottom: 1.4rem; }
  .proj-head { display: flex; justify-content: space-between; align-items: baseline; gap: 1rem; }
  .proj-title { font-weight: bold; }
  .proj-dates { white-space: nowrap; font-size: 0.85rem; color: var(--global-text-color-light); }
  .proj-role { color: var(--global-text-color-light); font-style: italic; }
  .proj-links a { margin-right: 0.4rem; font-size: 0.9rem; }
---

{% for group in site.data.projects %}

<h2>{% if group.source_url %}<a href="{{ group.source_url }}">{{ group.source }}</a>{% else %}{{ group.source }}{% endif %}</h2>

{% for p in group.projects %}

<div class="proj">
  <div class="proj-head"><span class="proj-title">{{ p.title }}</span><span class="proj-dates">{{ p.dates }}</span></div>
  <div class="proj-role">{{ p.role }}</div>
  <div>{{ p.description }}</div>
  <div class="proj-links">{% if p.code %}<a href="{{ p.code }}">[code]</a>{% endif %}{% if p.page %}<a href="{{ p.page }}">[page]</a>{% endif %}{% if p.video %}<a href="{{ p.video }}">[video]</a>{% endif %}</div>
</div>
{% endfor %}
{% endfor %}
