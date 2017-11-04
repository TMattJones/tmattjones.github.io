---
layout: page
title: Papers and Patents
permalink: /papers/
---

* Table of contents
{:toc}

My [Google Scholar](http://scholar.google.co.uk/citations?hl=en&user=oT8RhJgAAAAJ)
and
[DBLP](http://dblp.uni-trier.de/pers/hd/r/Reid:Alastair_David)
pages.

## Papers

{% for paper in site.data.biblio %}
  <div class="biblio">
    <a class="papertitle" href="{{ site.baseurl }}/papers/{{ paper.file }}">{{ paper.title }}</a>
    <br>
    {{ paper.author }},
    <br>
    {% if paper.booktitle %} In <i>{{ paper.booktitle }}</i>, {% endif %}
    {% if paper.acceptance %} {{ paper.acceptance }}% acceptance rate, {% endif %}
    {% if paper.journal %} {{ paper.journal }}, {% endif %}
    {% if paper.number %} {{ paper.number }}, {% endif %}
    {% if paper.publisher %} {{ paper.publisher }}, {% endif %}
    {% if paper.pages %} pp. {{ paper.pages }}, {% endif %}
    {{ paper.month }} {{ paper.year }}.
    {% if paper.doi %} doi: <a href="{{ paper.link }}">{{ paper.doi }}</a>
    {% elsif paper.link %} url: <a href="{{ paper.link }}">{{ paper.link }}</a>
    {% endif %}
    {% if paper.slides %} <br><a class="paperslides" href="{{ site.baseurl }}/papers/{{ paper.slides }}">slides</a> {% endif %}
    <br>
    <br>
  </div>
{% endfor %}

## Talks

{% for paper in site.data.talks %}
  <div class="biblio">
    <a class="papertitle" href="{{ site.baseurl }}/papers/{{ paper.slides }}">{{ paper.title }}</a>
    <br>
    {% if paper.link %}
        <a href="{{ paper.link }}">{{ paper.venue }}</a>
    {% else %}
        {{ paper.venue }},
    {% endif %}
    <br>
    {{ paper.city }},
    {{ paper.day }} {{ paper.month }}, {{ paper.year }}.
    <br>
    <br>
  </div>
{% endfor %}

## Patents

{% for paper in site.data.patents %}
  <div class="biblio">
    {% if paper.link %} <a href="{{ paper.link }}">{{ paper.title }}</a>
    {% else %} {{ paper.title }} {% endif %}
    <br>
    {{ paper.author }},
    <br>
    {{ paper.note }},
    <br>
    {{ paper.year }}.
    <br>
    <br>
  </div>
{% endfor %}
