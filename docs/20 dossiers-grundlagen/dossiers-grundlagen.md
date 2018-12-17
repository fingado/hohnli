---
layout: default
title: Dossiers Grundlagen
nav_order: 20
has_children: true
permalink: /docs/dossiers-grundlagen
---

# Dossiers zu Grundlagenthemen

Die Grundlagendossiers geben zu ganz unterschiedlichen Themen eine kurze Einführung mit Theorie und Beispielen. Dossiers
dienen zudem auch als Dokumentation, auf die jederzeit zugegriffen werden kann.
{: .fs-6 .fw-300 }

---
{% if page.has_children == true %}
## Übersicht über alle Dossiers
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
