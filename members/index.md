---
layout: article
title: Members
---

<div class="lab-hero">
  <h1 class="lab-title">Our Team</h1>
  <p class="lab-subtitle">Meet the researchers advancing multimodal auditory intelligence and robotics</p>
</div>
{%- for _pairs in site.data.members -%}
{%- assign _category = _pairs[0] -%}
<h2>{{ _category }}</h2>
<div class="author-profiles">
{%- assign _members = _pairs[1] -%}
{%- for _member in _members -%}
{%- assign _author = site.data.authors[_member] -%}
{%- include article/footer/author-profile.html path=_author -%}
{%- endfor -%}
</div>
{%- endfor -%}
