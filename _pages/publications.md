---
permalink: /publications/
title: "Publications"
description: "Publications and awards of Marco Balduini: journal and conference papers, tutorials and book chapters, with DOI and BibTeX links."
toc: true
toc_label: "Publications"
toc_sticky: true
---

{% assign profiles = "DBLP,ORCID,Google Scholar" | split: "," -%}
<p class="pub-profiles">
{%- for link in site.author.links -%}
  {%- if profiles contains link.label %}
  <a href="{{ link.url }}" class="btn btn--inverse btn--small"><i class="{{ link.icon }}" aria-hidden="true"></i> {{ link.label }}</a>
  {%- endif -%}
{%- endfor %}
</p>

## Awards
{: #awards}

- **IEEE MultiMedia Best Paper Award 2016** — "[CitySensing: Fusing City Data for Visual Storytelling](#ieee-mm-2015)"
- **Semantic Web Challenge 2011** — First place (BOTTARI)
- **Semantic Web Challenge 2012** — Finalist (crowd tracking during the London 2012 Opening Ceremony)
- **AI Mashup Challenge 2013 (ESWC)** — Third place (Social listening of Fuorisalone 2013)

## PhD Thesis
{: #phd-thesis}

{% include publications.html type="thesis" %}

## Journal Papers
{: #journal-papers}

{% include publications.html type="journal" by_year=true %}

## Conference Papers
{: #conference-papers}

{% include publications.html type="conference" by_year=true %}

## Tutorials
{: #tutorials}

{% include publications.html type="tutorial" %}

## Book Chapters
{: #book-chapters}

{% include publications.html type="chapter" %}
