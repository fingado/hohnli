---
layout: default
title: Einfaches Zeichnen und Schreiben
parent: Programmieren mit der Turtle

nav_order: 1
---
<div class="text-red-000">
<em><font size="1"><b>Achtung:</b> auf dieser Seite befinden sich eingebettete Plugins von trinket.io zum direkten Anwenden von Programmiercode im Browser. Das ist ziemlich praktisch um das Programmieren zu erlernen, aber leider zeichnet trinket.io dein Surfverhalten auf und gibt diese Informationen unter Umständen an Dritte weiter. <a href="https://www.hohn.li/docs/datenschutz"><b>Lerne, wie du dich dagegen schützen kannst.</b></a></font></em>
</div>
---
# Zeichnen mit der Turtle
---

Unsere Schildkröte Anton kann sich aufgrund von unseren Anweisungen auf der Bildschirmfläche bewegen. Bei jeder Bewegung zeichnet Anton eine Linie. Anton kann sich vorwärts (forward) und rückwärts (backward) bewegen:

```python
forward(distanz)
backward(distanz)
```

In die Klammern muss ein Parameter eigegeben werden. Ein Parameter ist in diesem Fall eine Zahl, welche die Distanz beschreibt, die Anton gehen soll.

Anton kann sich zudem nach rechts (right) oder links (left) bewegen:

```python
right(winkel)
left(winkel)
```

In die Klammern muss wieder ein Parameter eigegeben werden, dieses Mal aber ein Winkel in Grad (zum Anfangen am besten mit Werten zwischen 0° und 360° experimentieren!).

Führe den untenstehenden Code aus und versuche ihn danach zu manipulieren, indem du die Schildkröte dazu bringst, ein Dreieck zu zeichnen. Versuche danach eine Figur zu zeichnen (Dreieck, Viereck, Fünfeck...), bei der sich die Schildkröte **nur** rückwärts bewegt.



>_Wichtig ist, dass bei jedem Befehl spezifiziert wird, dass Anton ihn ausführen muss. Vor jeder Anweisung muss also Anton (unser Objekt) stehen, indem der Name von Anton angegeben wird, gefolgt von einem Punkt und dem zu verwendenden Befehl:_

> _Anton.Befehl_  


{% raw %}
<br>
<iframe src="https://trinket.io/embed/python/8c9decb0f8" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
{% endraw %}

---

# Schreiben mit der Turtle

---

Anton kann auch schreiben. Mit dem Befehl

```python
write("text")
```

schreibt Anton den in der Klammer angegebenen Text. Dies tut er immer an der Stelle, wo er sich gerade befindet. Führe das untenstehende Beispiel aus und versuche, den von Anton geschriebenen Text zu verändern. Zum Beispiel mit deinem Namen.

{% raw %}
<iframe src="https://trinket.io/embed/python/dfbe199583" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
{% endraw %}

---

# Die Position der Turtle und bewegen ohne Stift

---

Das Fenster in dem Anton sich bewegt müssen wir uns wie ein Koordinatensystem vorstellen. Für unsere Zwecke ist das Koordinatensystem von Anton begrenzt auf 400x400 Pixel. Wir können uns das so vorstellen, dass Anton in der Mitte des Fensters startet (bei (x = 0 / y = 0)) und 200 Schrite nach links und 200 Schritte nach rechts gehen kann, so dass vom linken Fensterrand bis zum rechten Fensterrand maximal 400 Schritte möglich sind. Der folgende Code-Ausschnitt versucht das darzustellen. Führe den Code aus und versuche das Koordinatensystem zu verstehen.

{% raw %}
<iframe src="https://trinket.io/embed/python/7ef2012de4" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
{% endraw %}

Im Code Ausschnitt von oben sind einige neue Funktionen ersichtlich. Erstens können wir den Stift von Anton entweder anheben, oder ablegen. Anheben (**penup()**) heisst, dass Anton gar nichts zeichnen soll, auch wenn er sich bewegt. Ablegen (**pendown()**) heisst, dass Anton etwas zeichnen soll:

```python
penup()
pendown()
```

Eine weitere Funktion im obenstehenden Code ist **goto()**. Mit **goto()** können wir Anton irgendwohin in unserem Koordinatensystem schicken. In die Klammern müssen wir lediglich die Koordinaten eingeben. Mögliche Koordinaten sind -200 bis 200. X und Y Koordinaten müssen mit einem Komma getrennt werden.

```python
goto(x,y)
```

Eine weitere Funktion im obenstehenden Code ist **speed()**. Damit können wir die Geschwindigkeit von Anton beeinflussen. Die Geschwindigkeit kann Werte zwischen 0 und 10 annehmen. Ein Wert von 1 führt dazu, dass Anton sich sehr langsam bewegt, ein Wert von 10 macht Anton sehr schnell. Achtung: ein Wert von 0 bedeutet, dass Antons Animation ausser Kraft gesetzt wird. Die Turtle bewegt sich dadurch (unter Umständen) noch schneller als mit 10.

```python
speed(geschwindigkeit)
```

Weiterhin wurde im Code die Farbe von Anton gewechselt. Die Farbe beeinflusst sowohl die Linien, die Anton zeichnet, als auch den Text, den Anton schreibt. Die Funktion dafür ist **color()** und als Argument für die Funktion muss eine Farbe eingesetzt werden. Alle gängigen Farben gehen dafür, sie müssen aber auf Englisch und in ANführungszeichen angegeben werden:

```python
color("farbe")   # zum Beispiel "green", "blue" oder "red"
```

Die letzte verwendetet Funktion war **hideturtle()**. Diese Funktion versteckt Anton.

```python
hideturtle()
```
---

# Übersicht aller bisher verwendeten Funktionen

---

Um ein Turtle-Programm in Python starten zu können, müssen wir immer folgenden Code-Block ausführen (wir werden ihn später noch verstehen lernen):

```python
import turtle             # Turtle Bibliothek von Python importieren
window = turtle.Screen()  # Fenster initialisieren (nötig)
Anton = turtle.Turtle()   # ein neues Objekt generieren: eine Turtle namens Anton
Anton.shape("turtle")     # Anton soll das Aussehen einer Schildkröte haben.
```

Wichtig ist zudem, vor jede Funktion immer unser Objekt zu platzieren. Unser Objekt heisst Anton. Wir schreiben also immer _Anton.funktion(argument)_ um eine Funktion auszuführen.

Bisher verwendete Funktionen (mögliche Argumente in Klammern):

```python
forward(distance)   # Distanz als Zahl
backward(distance)  # Distanz als Zahl
right(arc)          # arc = Winkel als Zahk
left(arc)           # arc = Winkel als Zahl
write("text")       # Text in Anführungszeichen!
penup()             # kein Argument!
pendown()           # kein Argument!
goto(x,y)           # x- und y-Koordinaten als Zahlen, getrennt mit Komma.
speed(value)        # Wert zwischen 0 und 10
color("farbe")   # zum Beispiel "green", "blue" oder "red"
hideturtle()        # kein Argument!
```


---

# Übungen

---
