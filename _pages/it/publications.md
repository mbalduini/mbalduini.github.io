---
ref: publications
permalink: /it/publications/
title: "Pubblicazioni"
description: "Pubblicazioni e premi di Marco Balduini: articoli su rivista e a conferenza, tutorial e capitoli di libro, con link a DOI e BibTeX."
toc: true
toc_label: "Pubblicazioni"
toc_sticky: true
---

{% assign profiles = "DBLP,ORCID,Google Scholar" | split: "," -%}
<p class="pub-profiles">
{%- assign author = site.data.authors[page.author] | default: site.data.authors.en -%}
{%- for link in author.links -%}
  {%- if profiles contains link.label %}
  <a href="{{ link.url }}" class="btn btn--inverse btn--small"><i class="{{ link.icon }}" aria-hidden="true"></i> {{ link.label }}</a>
  {%- endif -%}
{%- endfor %}
</p>

## Premi
{: #awards}

- **IEEE MultiMedia Best Paper Award 2016** — "[CitySensing: Fusing City Data for Visual Storytelling](#ieee-mm-2015)"
- **Semantic Web Challenge 2011** — primo posto (BOTTARI)
- **Semantic Web Challenge 2012** — finalista (tracciamento della folla durante la cerimonia di apertura di Londra 2012)
- **AI Mashup Challenge 2013 (ESWC)** — terzo posto (social listening del Fuorisalone 2013)

## Tesi di dottorato
{: #phd-thesis}

{% include publications.html type="thesis" %}

## Articoli su rivista
{: #journal-papers}

{% include publications.html type="journal" by_year=true %}

## Articoli a conferenza
{: #conference-papers}

{% include publications.html type="conference" by_year=true %}

## Tutorial
{: #tutorials}

{% include publications.html type="tutorial" %}

## Capitoli di libro
{: #book-chapters}

{% include publications.html type="chapter" %}
