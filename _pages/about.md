---
layout: about
title: About
permalink: /
subtitle: '<span class="hero-role">C.S. Bachelor Student &amp; MIR Researcher</span><br><span class="hero-aff">Undergrad. Researcher @ <a href="https://labic.icmc.usp.br/index.html">LABIC</a>, <a class="has-tip" href="https://www5.usp.br/" data-tip="University of São Paulo: Brazil&#39;s top-ranked university and #2 in Latin America (QS Latin America &amp; The Caribbean 2027). #71 in the world for Computer Science (QS World University Rankings by Subject 2026).">USP</a></span>'

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <div class="profile-icons">
    <a href="mailto:lucasouza@usp.br" title="Email"><i class="fa-solid fa-envelope"></i></a>
    <a href="https://github.com/sb-lucas" title="GitHub" target="_blank"><i class="fa-brands fa-github"></i></a>
    <a href="https://www.linkedin.com/in/sb-lucas" title="LinkedIn" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
    <a href="http://lattes.cnpq.br/9012679553527210" title="Lattes" target="_blank"><i class="ai ai-lattes"></i></a>
    <a href="https://orcid.org/0009-0002-1426-8617" title="ORCID" target="_blank"><i class="ai ai-orcid"></i></a>
    </div>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # social icons are shown under the photo instead (profile.more_info)

announcements:
  enabled: false # news is rendered below as a timeline

latest_posts:
  enabled: false

---

<div class="info-grid">
  <div><span class="info-label">Birthday</span>June 1st, 2004</div>
  <div><span class="info-label">Age</span>22</div>
  <div><span class="info-label">City</span>São Carlos, Brazil</div>
  <div><span class="info-label">Degree</span>Undergraduate</div>
</div>

I am a Bachelor's student in Computer Science at <a href="https://icmc.usp.br/">ICMC-USP</a>, in the <a href="https://labic.icmc.usp.br/index.html">LABIC</a> lab, advised by [Prof. Dr. Diego Furtado Silva](https://scholar.google.com/citations?user=HXu5lB4AAAAJ&hl=en).

My research focuses on Music Information Retrieval (MIR), especially representation learning for musical data. Recently, I have been particularly interested in controllable and multimodal music similarity retrieval and recommendation.

Previously, I was a visiting researcher at the [Music Technology Group (MTG)](https://www.upf.edu/web/mtg) at Universitat Pompeu Fabra, Barcelona.

<style>
.has-tip { position: relative; text-decoration: underline dotted; text-decoration-color: var(--global-text-color-light); text-underline-offset: 3px; cursor: help; }
.has-tip:hover::after { content: attr(data-tip); position: absolute; left: 0; top: 1.6rem; z-index: 10; width: 18rem; padding: 0.5rem 0.7rem; font-size: 0.8rem; line-height: 1.35; color: var(--global-text-color); background: var(--global-bg-color); border: 1px solid var(--global-divider-color); border-radius: 4px; box-shadow: 0 2px 8px rgba(0,0,0,0.25); }
.hero-role { font-size: 1.15rem; font-weight: 500; }
.hero-aff { color: var(--global-text-color-light); }
.info-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 0.5rem 1.5rem; margin: 0.5rem 0 1.5rem; }
.info-label { display: inline-block; min-width: 5.5rem; margin-right: 0.6rem; padding-right: 0.6rem; border-right: 2px solid var(--global-theme-color); font-weight: 600; text-align: right; }
@media (max-width: 576px) { .info-grid { grid-template-columns: 1fr; } }
.profile-icons { display: flex; justify-content: center; gap: 0.9rem; font-size: 1.5rem; margin-top: 0.6rem; }
.profile-icons a { color: var(--global-text-color) !important; }
.profile-icons a:hover { color: var(--global-theme-color) !important; }
.news-year { font-size: 1.6rem; font-weight: 300; margin: 1rem 0 0.6rem; }
.news-tl { position: relative; margin-left: 4.5rem; border-left: 1px solid var(--global-divider-color); padding-left: 1.4rem; }
.news-tl-item { position: relative; margin-bottom: 1.1rem; }
.news-tl-item::before { content: ""; position: absolute; left: calc(-1.4rem - 4px); top: 0.45rem; width: 7px; height: 7px; border-radius: 50%; border: 1px solid var(--global-theme-color); background: var(--global-bg-color); }
.news-tl-date { position: absolute; left: -5.9rem; width: 3.6rem; text-align: right; top: 0.1rem; font-size: 0.85rem; color: var(--global-theme-color); }
.news-heading { clear: both; padding-top: 1rem; }
</style>

<h2 class="news-heading">News</h2>

{% assign news = site.news | reverse %}
{% assign current_year = "" %}
{% for item in news limit: 6 %}
{% assign y = item.date | date: "%Y" %}
{% if y != current_year %}
{% unless forloop.first %}</div>{% endunless %}
<div class="news-year">{{ y }}</div>
<div class="news-tl">
{% assign current_year = y %}
{% endif %}
<div class="news-tl-item"><span class="news-tl-date">{{ item.date | date: "%m.%d" }}</span>{{ item.content | remove: '<p>' | remove: '</p>' }}</div>
{% endfor %}
{% if news.size > 0 %}</div>{% endif %}
