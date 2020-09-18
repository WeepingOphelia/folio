---
layout: page
title: Writing
permalink: /writing/
---

## NON-FICTION

<ul class="post-list">
  {%- for post in site.posts -%}
  {%- if post.genre == "xfict" -%}
  <li>
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    <span class="post-meta">{{ post.date | date: date_format }}</span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    {%- if site.show_excerpts -%}
      {{ post.excerpt }}
    {%- endif -%}
  </li>
  {%- endif -%}
  {%- endfor -%}
</ul>

## FICTION

<ul class="post-list">
  {%- for post in site.posts -%}
  {%- if post.genre == "fict" -%}
  <li>
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    <span class="post-meta">{{ post.date | date: date_format }}</span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    {%- if site.show_excerpts -%}
      {{ post.excerpt }}
    {%- endif -%}
  </li>
  {%- endif -%}
  {%- endfor -%}
</ul>
