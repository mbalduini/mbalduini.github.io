---
permalink: /contact/
title: "Contact"
---

For collaborations, projects or training, the best way to reach me is email or LinkedIn.

<ul class="contact-links">
{%- for link in site.author.links %}
  {%- assign is_mail = false %}
  {%- if link.url contains "mailto:" %}{% assign is_mail = true %}{% endif %}
  {%- assign shown = link.display | default: link.url | remove: "mailto:" | remove: "https://" | remove: "http://" | remove: "www." | remove: ".html" %}
  <li>
    <i class="{{ link.icon }}" aria-hidden="true"></i>
    <span class="contact-links__label">{{ link.label }}</span>
    <a href="{{ link.url }}"{% unless is_mail %} target="_blank" rel="noopener noreferrer"{% endunless %}>{{ shown }}</a>
  </li>
{%- endfor %}
</ul>
