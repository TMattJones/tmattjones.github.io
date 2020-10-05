---
layout: page
title: Papers, Talks and Patents
permalink: /papers/
---

* Table of contents
{:toc}

## Papers

<table>
{% for paper in site.data.biblio %}
    <tr style="vertical-align:top">
        <td class="bibtexnumber" style="text-align:right; padding: 10px;">
            <a class="papertitle" href="{{ site.baseurl }}/papers/{{ paper.ar_file }}">{{ paper.ar_shortname | replace:' ','&nbsp;'}}</a>
        </td>
        <td class="bibtexitem">
            {{ paper.ar_title }}
        </td>
    </tr>
{% endfor %}
</table>
