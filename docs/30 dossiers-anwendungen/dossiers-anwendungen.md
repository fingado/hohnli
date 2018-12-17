---
layout: default
title: Dossiers Anwendungen
nav_order: 30
has_children: true
permalink: /docs/dossiers-anwendungen
---

# Dossiers zu Anwendungen

Bei den Anwendungsdossiers handelt es sich um eine Einführung in wichtige Anwendungen. Es werden die Grundlagen ausgewählter Anwendungen besprochen und teilweise konkrete weiterführende Funktionen behandelt. Diese Dossiers dienen zudem auch als Dokumentation, auf die jederzeit zugegriffen werden kann.
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
