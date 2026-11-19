---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 5
cv_pdf: /files/cv.pdf
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
  .post-header { display: none; }
  .cv-top { display: grid; grid-template-columns: 2fr 1fr; gap: 2rem; margin: 1rem 0 2rem; }
  .cv-top h2 { margin-top: 0; }
  .cv-skill-row { display: flex; gap: 1rem; align-items: baseline; margin-bottom: 0.6rem; }
  .cv-skill-row:last-child { margin-bottom: 0; }
  .cv-skill-label { flex: 0 0 6.5rem; color: var(--global-text-color-light); font-size: 0.9rem; }
  .cv-chips { display: flex; flex-wrap: wrap; gap: 0.35rem; }
  .cv-chip { padding: 0.1rem 0.55rem; font-size: 0.82rem; border: 1px solid var(--global-divider-color); border-radius: 999px; }
  .cv-side { display: flex; flex-direction: column; align-items: flex-start; }
  .cv-skills { display: flex; flex-direction: column; }
  .cv-langs { list-style: none; padding: 0; margin: 0; width: 100%; flex: 1; display: flex; flex-direction: column; justify-content: space-between; }
  .cv-langs li { display: flex; justify-content: space-between; padding: 0 0 0.3rem; border-bottom: 1px solid var(--global-divider-color); }
  .cv-lang-level { color: var(--global-text-color-light); font-size: 0.9rem; }
  @media (max-width: 576px) { .cv-top { grid-template-columns: 1fr; } .cv-skill-row { flex-direction: column; gap: 0.3rem; } .cv-skill-label { flex: none; } }
  .cv-download-row { display: flex; justify-content: flex-end; margin-bottom: 1rem; }
  .cv-download { display: inline-flex; align-items: center; gap: 0.5rem; padding: 0.4rem 0.9rem; font-size: 0.9rem; line-height: 1; border: 1px solid var(--global-theme-color); border-radius: 4px; color: var(--global-theme-color) !important; }
  .cv-download:hover { background: var(--global-theme-color); color: #fff !important; text-decoration: none; }
---

{% assign cv = site.data.cv.cv %}

<div class="cv-download-row"><a class="cv-download" href="/files/cv.pdf" target="_blank"><i class="fa-solid fa-download"></i><span>Download PDF</span></a></div>

{% for section in cv.sections %}
{% assign name = section[0] %}
{% if name == "Skills" or name == "Languages" %}{% continue %}{% endif %}

## {{ name }}



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
      <span class="timeline-date">{{ item.start_date | append: "-01" | date: "%b %Y" }} – {% if item.end_date == "present" %}Present{% else %}{{ item.end_date | append: "-01" | date: "%b %Y" }}{% if item.expected %} (expected){% endif %}{% endif %}</span>
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

{% endfor %}

<div class="cv-top">
  <div class="cv-skills">
    <h2>Skills</h2>
    {% for item in cv.sections.Skills %}
    <div class="cv-skill-row">
      <span class="cv-skill-label">{{ item.name }}</span>
      <div class="cv-chips">{% assign kws = item.keywords | split: ", " %}{% for k in kws %}<span class="cv-chip">{{ k }}</span>{% endfor %}</div>
    </div>
    {% endfor %}
  </div>
  <div class="cv-side">
    <h2>Languages</h2>
    <ul class="cv-langs">
      {% for item in cv.sections.Languages %}<li><span>{{ item.name }}</span><span class="cv-lang-level">{{ item.summary }}</span></li>{% endfor %}
    </ul>
  </div>
</div>
