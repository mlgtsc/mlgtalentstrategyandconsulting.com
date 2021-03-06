---
title: Stats
layout: default
---

# Site Statistics


|Page Title(path) | Hits | uniqID |
|:----------|:-------|:-----|
{%- for p in site.pages -%}
 {%- assign hitID =  p.hitID | default: p.dir|replace: "/","_" | append: p.name | strip | replace: " ","" | downcase| prepend: "page_"  %}
| {{ p.hitID | default: p.title }}({{p.dir}}{{p.name}}) |  <img src="https://hitcounter.pythonanywhere.com/nocount/tag.svg?url={{ site.github_url | append: 'hit-counter-' | append: hitID | url_encode }}" alt="Users"> | {{ hitID|url_encode }} |
{%- endfor %}

## Raw links

{%- for p in site.pages -%}
 {%- assign hitID =  p.hitID | default: p.dir|replace: "/","_" | append: p.name | strip | replace: " ","" | downcase| prepend: "page_"  %}
<br>
https://hitcounter.pythonanywhere.com/nocount/tag.svg?url={{ site.github_url | append: 'hit-counter-' | append: hitID | url_encode }}
{%- endfor %}
