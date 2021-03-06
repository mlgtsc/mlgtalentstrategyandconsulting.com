---
title: Stats
---

# Site Statistics


|Page Title(path) | uniqID | Hits |
|:----------|:-------|:-----|
{%- for p in site.pages -%}
 {%- assign hitID =  p.hitID | default: p.title | strip | replace: " ","" | downcase| prepend: "page_"  %}
| {{ p.title }}({{p.dir}}) |{{ hitID }} |  <img src="https://hitcounter.pythonanywhere.com/nocount/tag.svg?url={{ site.github_url | append: 'hit-counter-' | append: hitID | url_encode }}" alt="Users"> |
{%- endfor %}
