---
permalink: /contact/
title: "Contact"
---

For collaborations, projects or training, the best way to reach me is email or LinkedIn.

<ul class="contact-links">
{%- for link in site.author.links %}
  <li><a href="{{ link.url }}"><i class="{{ link.icon }}" aria-hidden="true"></i>{{ link.label }}</a>{% if link.url contains "mailto:" %} — {{ link.url | remove: "mailto:" }}{% endif %}</li>
{%- endfor %}
</ul>
