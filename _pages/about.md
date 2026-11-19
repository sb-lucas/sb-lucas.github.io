---
layout: about
title: About
permalink: /
subtitle: '<span class="hero-role">C.S. Bachelor Student &amp; MIR Researcher</span><br><span class="hero-aff">Undergrad. Researcher @ <a href="https://labic.icmc.usp.br/index.html">LABIC</a>, <a class="has-tip" href="https://www5.usp.br/" data-tip="University of São Paulo: Brazil&#39;s top-ranked university and #2 in Latin America (QS Latin America &amp; The Caribbean 2027). #71 in the world for Computer Science (QS World University Rankings by Subject 2026).">USP</a></span>'

profile:
  align: left
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <div class="profile-icons">
    <a href="mailto:lucasouza@usp.br" title="Email"><i class="fa-solid fa-envelope"></i></a>
    <a href="https://scholar.google.com/citations?user=26A2DXoAAAAJ&hl=en" title="Google Scholar" target="_blank"><i class="ai ai-google-scholar"></i></a>
    <a href="https://www.linkedin.com/in/sb-lucas" title="LinkedIn" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
    <a href="https://github.com/sb-lucas" title="GitHub" target="_blank"><i class="fa-brands fa-github"></i></a>
    <a href="https://orcid.org/0009-0002-1426-8617" title="ORCID" target="_blank"><i class="ai ai-orcid"></i></a>
    <a href="http://lattes.cnpq.br/9012679553527210" title="Lattes" target="_blank"><i class="ai ai-lattes"></i></a>
    </div>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # social icons are shown under the photo instead (profile.more_info)

announcements:
  enabled: false # news is rendered below as a timeline

latest_posts:
  enabled: false

---

<div class="bio-card" markdown="1">

<div class="bio-head">
  <h2 class="bio-title">About me</h2>
  <div class="bio-toggle" role="group" aria-label="Bio">
    <button type="button" data-bio="professional" class="active">Work</button>
    <button type="button" data-bio="personal">Life</button>
  </div>
</div>

<div class="bio-professional" markdown="1">

I am a Bachelor's student in Computer Science at <a href="https://icmc.usp.br/">ICMC-USP</a>, in the <a href="https://labic.icmc.usp.br/index.html">LABIC</a> lab, advised by [Prof. Dr. Diego Furtado Silva](https://scholar.google.com/citations?user=HXu5lB4AAAAJ&hl=en). Previously, I was a visiting researcher at the [Music Technology Group (MTG)](https://www.upf.edu/web/mtg) at Universitat Pompeu Fabra, Barcelona.

My research focuses on Music Information Retrieval (MIR), especially representation learning for musical data. Recently, I have been particularly interested in controllable and multimodal music similarity retrieval and recommendation.

</div>

<div class="bio-personal" markdown="1">

I am a very curious person. My hobbies span a wide range of interests, so I am always learning about some random topic. Among them, I like cooking, fashion, gaming, martial arts, sociology, music, and whatever I'm interested in at the moment.

Music, in particular, has always been part of my life. My earliest memory is of my father listening to [Charlie Brown Jr.](https://www.youtube.com/watch?v=45YuWYQ1YkE) on his computer. I have played the electric guitar since I was 11, and I have also tried a little bit of singing and music production.

</div>

</div>

<style>
.bio-card { overflow: hidden; margin-bottom: 1.5rem; }
.bio-card .bio-professional, .bio-card .bio-personal { padding: 0.8rem 0 0; }
.bio-head { display: flex; justify-content: space-between; align-items: center; }
.bio-title { margin: 0; }
.bio-toggle button:last-child { padding-right: 0; }
.bio-toggle { display: flex; }
.bio-toggle button { border: 0; padding: 0.35rem 1rem; font-size: 0.85rem; background: transparent; color: var(--global-text-color-light); cursor: pointer; }
.bio-toggle button.active { color: var(--global-text-color); font-weight: 600; box-shadow: inset 0 -2px 0 var(--global-theme-color); }
.bio-personal { display: none; }
.bio-card.show-personal .bio-personal { display: block; }
.bio-card.show-personal .bio-professional { display: none; }
.has-tip { position: relative; text-decoration: underline dotted; text-decoration-color: var(--global-text-color-light); text-underline-offset: 3px; cursor: help; }
.has-tip:hover::after { content: attr(data-tip); position: absolute; left: 0; top: 1.6rem; z-index: 10; width: 18rem; padding: 0.5rem 0.7rem; font-size: 0.8rem; line-height: 1.35; color: var(--global-text-color); background: var(--global-bg-color); border: 1px solid var(--global-divider-color); border-radius: 4px; box-shadow: 0 2px 8px rgba(0,0,0,0.25); }
.hero-role { font-size: 1.15rem; font-weight: 500; }
.hero-aff { color: var(--global-text-color-light); }
.profile-icons { display: flex; justify-content: center; gap: 0.9rem; font-size: 1.5rem; margin-top: 0.6rem; }
.profile-icons a { color: var(--global-text-color) !important; }
.profile-icons a:hover { color: var(--global-theme-color) !important; }
.news-tl { position: relative; margin-left: 4.5rem; border-left: 1px solid var(--global-divider-color); padding-left: 1.4rem; }
.news-tl-item { position: relative; margin-bottom: 1.1rem; }
.news-tl-item::before { content: ""; position: absolute; left: calc(-1.4rem - 4px); top: 0.45rem; width: 7px; height: 7px; border-radius: 50%; border: 1px solid var(--global-theme-color); background: var(--global-bg-color); }
.news-tl-date { position: absolute; left: -5.9rem; width: 3.6rem; text-align: right; top: 0.1rem; font-size: 0.85rem; color: var(--global-theme-color); }
.news-section { clear: both; padding-top: 1.5rem; }
.news-head { display: flex; justify-content: space-between; align-items: center; margin-bottom: 1rem; }
.news-heading { margin: 0; }
.news-years button { border: 0; padding: 0.35rem 1rem; font-size: 0.85rem; background: transparent; color: var(--global-text-color-light); cursor: pointer; }
.news-years button:last-child { padding-right: 0; }
.news-years button.active { color: var(--global-text-color); font-weight: 600; box-shadow: inset 0 -2px 0 var(--global-theme-color); }
</style>

<script>
  document.querySelectorAll(".bio-toggle button").forEach(function (btn) {
    btn.addEventListener("click", function () {
      document.querySelectorAll(".bio-toggle button").forEach(function (b) { b.classList.toggle("active", b === btn); });
      document.querySelector(".bio-card").classList.toggle("show-personal", btn.dataset.bio === "personal");
    });
  });
</script>

<div class="news-section">

<div class="news-head">
  <h2 class="news-heading">News</h2>
  <div class="news-years" role="group" aria-label="Year">
  {% assign news = site.news | reverse %}
  {% assign years = "" %}
  {% for item in news %}{% assign y = item.date | date: "%Y" %}{% unless years contains y %}{% assign years = years | append: y | append: "," %}{% endunless %}{% endfor %}
  {% assign year_list = years | split: "," %}
  {% for y in year_list %}<button type="button" data-year="{{ y }}"{% if forloop.first %} class="active"{% endif %}>{{ y }}</button>{% endfor %}
  </div>
</div>

<div class="news-tl">
{% for item in news %}
{% assign y = item.date | date: "%Y" %}
<div class="news-tl-item" data-year="{{ y }}"{% if y != year_list[0] %} hidden{% endif %}><span class="news-tl-date">{{ item.date | date: "%m.%d" }}</span>{{ item.content | remove: '<p>' | remove: '</p>' }}</div>
{% endfor %}
</div>

</div>

<script>
  document.querySelectorAll(".news-years button").forEach(function (btn) {
    btn.addEventListener("click", function () {
      document.querySelectorAll(".news-years button").forEach(function (b) { b.classList.toggle("active", b === btn); });
      document.querySelectorAll(".news-tl-item").forEach(function (it) { it.hidden = it.dataset.year !== btn.dataset.year; });
    });
  });
</script>
