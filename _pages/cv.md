---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 5
cv_pdf: /assets/pdf/cv.pdf
description:
_styles: >
  .timeline { position: relative; margin: 0 0 2.5rem 0; padding-left: 1.75rem; border-left: 2px solid var(--global-divider-color); }
  .timeline-item { position: relative; margin-bottom: 1.75rem; }
  .timeline-item::before { content: ""; position: absolute; left: calc(-1.75rem - 7px); top: 0.35rem; width: 12px; height: 12px; border-radius: 50%; background: var(--global-bg-color); border: 2px solid var(--global-theme-color); }
  .timeline-item h4 { font-size: 1.05rem; margin: 0 0 0.15rem 0; }
  .timeline-head { display: flex; justify-content: space-between; align-items: baseline; gap: 1rem; }
  .timeline-date { white-space: nowrap; font-size: 0.85rem; color: var(--global-text-color-light); }
  .timeline-place { font-style: italic; color: var(--global-text-color-light); margin-bottom: 0.3rem; }
  .timeline-item ul { margin-bottom: 0; padding-left: 1.1rem; }
  .cv-list { padding-left: 1.1rem; }
  .cv-download { display: inline-block; padding: 0.45rem 1rem; border: 1px solid var(--global-theme-color); border-radius: 4px; color: var(--global-theme-color) !important; }
  .cv-download:hover { background: var(--global-theme-color); color: #fff !important; text-decoration: none; }
---

<p><a class="cv-download" href="/assets/pdf/cv.pdf" target="_blank" download><i class="fa-solid fa-file-pdf"></i> Download CV (PDF)</a></p>

{% assign cv = site.data.cv.cv %}

{% for section in cv.sections %}
{% assign name = section[0] %}

## {{ name }}

{% if name == "Skills" or name == "Languages" %}

<ul class="cv-list">
{% for item in section[1] %}
  <li><strong>{{ item.name }}:</strong> {{ item.keywords | default: item.summary }}</li>
{% endfor %}
</ul>

{% else %}

<div class="timeline">
{% for item in section[1] %}
  {% if name == "Student Groups" %}
    {% assign heading = item.company %}{% assign sub = item.position %}
  {% else %}
    {% assign heading = item.position | default: item.studyType %}{% if item.area %}{% assign heading = heading | append: " in " | append: item.area %}{% endif %}
    {% assign sub = item.company | default: item.institution %}
  {% endif %}
  <div class="timeline-item">
    <div class="timeline-head">
      <h4>{% if name == "Student Groups" and item.url %}<a href="{{ item.url }}">{{ heading }}</a>{% else %}{{ heading }}{% endif %}</h4>
      <span class="timeline-date">{{ item.start_date | append: "-01" | date: "%b %Y" }} – {% if item.end_date == "present" %}Present{% else %}{{ item.end_date | append: "-01" | date: "%b %Y" }}{% endif %}</span>
    </div>
    <div class="timeline-place">{% if name != "Student Groups" and item.url %}<a href="{{ item.url }}">{{ sub }}</a>{% else %}{{ sub }}{% endif %}{% if item.location %}, {{ item.location }}{% endif %}</div>
    {% if item.summary %}<p>{{ item.summary }}</p>{% endif %}
    {% if item.highlights %}
    <ul>
      {% for h in item.highlights %}<li>{{ h }}</li>{% endfor %}
    </ul>
    {% endif %}
    {% if item.transcript %}<p><a href="{{ item.transcript }}" target="_blank"><i class="fa-solid fa-file-pdf"></i> Check my academic transcript</a></p>{% endif %}
  </div>
{% endfor %}
</div>

{% endif %}
{% endfor %}
