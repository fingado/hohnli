---
layout: default
title: Datenschutz
nav_order: 80
has_children: true
permalink: docs/datenschutz
---

# Datenschutz
{:.no_toc}

Die folgenden Seiten gehen im Details auf das Thema Datenschutz ein. Es wird erläutert, wie sich Konsumentendaten zur Grundlage eines neuen Business-Modells im Internet entwickelt haben. Usw. usf.
{: .fs-6 .fw-300 }

---
{% if page.has_children == true %}
## Inhaltsverzeichnis
{% assign children_list = site.pages | sort:"nav_order" %}
<ul>
  {% for child in children_list %}
    {% if child.parent == page.title and child.title != page.title %}
    <li>
      <a href="{{ child.url | absolute_url }}">{{ child.title }}</a>
    </li>
    {% endif %}
  {% endfor %}
</ul>
{% endif %}
---
