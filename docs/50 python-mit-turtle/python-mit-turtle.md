---
layout: default
title: Programmieren mit der Turtle
nav_order: 50
has_children: true
permalink: /docs/programmieren-mit-turtle
---

# Python mit der Turtle

Programmieren lernen mit einer Turtle hat lange Tradition. Es geht dabei darum, eine Schildkröte mit Hilfe von Programmier-Anweisungen zu bewegen. Untenstehend befindet sich ein Fenster mit einer Schildkröte und einigen Programmieranweisungen. Finde dich im Fenster zurecht und Versuche den Code auszuführen. Wenn das geklappt hat, versuche den Code zu verändern, so, dass die Turtle etwas anderes macht.
{: .fs-6 .fw-300 }

{% raw %}
<iframe src="https://trinket.io/embed/python/6542d6ad42" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
{% endraw %}  
Die im obenstehenden Beispiel verwendete und vorgestellte Programmiersprache heisst **Python**. Es gibt unzählige verschiedene Programmiersprachen, Python ist aber sehr verbreitet und verhältnismässig einfach, weshalb sich Python sehr gut als Einstieg in die Welt des Programmierens eignet. Die folgenden Übungen führen in das Programmieren mit der Python-Turtle ein. Untenstehend ist eine Übersicht aller Lektionen, es empfiehlt sich, der Reihe nach durchzugehen.

---
{% if page.has_children == true %}
## Übersicht über alle Lektionen zum Programmieren in Python mit der Turtle
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
