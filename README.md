# Calliope Funk Pong
<hr>

## Werkzeuge
<hr>

* Laptop
* Online Entwicklungsumgebung: https://pxt.calliope.cc/
* 2 x Mikrocontroller 'Calliope mini'
* USB Kabel zur Datenübertragung zwischen Calliope und Laptop
* Stromquelle für den Calliope
* Batterien

## Das Spiel
<hr>

Herzlich Willkommen!
In diesem Abschnitt stellt ihr euch der Herausforderung den Spielklassiker Pong (https://de.wikipedia.org/wiki/Pong) zu programmieren!

Wir wollen euch damit die Möglichkeit geben das Programmieren auf einfache aber auch sehr interessante
Weise zu erlernen. Ihr werdet lernen den Calliope mini und eine dazugehörige Entwicklungsumgebung, die
ihr online abrufen könnt, zu benutzen. Während ihr euch mit der Calliope Plattform vertraut macht, lernt
ihr die verschiedenen Bausteine kennen, aus denen wirklich jedes Computerprogramm besteht. Nicht zu
vergessen, setzt ihr die Spiellogik für das oben genannte Pong Spiel um und könnt am Ende auf ein fertiges
Spiel schauen, dass ihr selbst programmiert habt!

Knifflig wir es dann, wenn ihr eure Spiellogik anpassen müsst, da sich das Spiel nicht so verhält wie gewünscht.
Aber keine Angst, das ist ein Teil der Herausforderung und wird euch dazu bringen über euren Code genauer
nachzudenken.

Das Spiel soll wie folgt aussehen:

[GIF MIT FERTIGEM SPIEL]

Das Spiel startet, indem zwei Calliopes angeschaltet werden und ein Mitspieler die B-Taste drückt. Daraufhin
erscheint ein Ball und der Spielerbalken in der Mitte der Anzeigefläche dieses Spielers. Der Ball soll sich automatisch anfangen zu
bewegen. Mithilfe des Spielerbalkens kann man den Ball abwehren. Es verliert der Mitspieler, der zuerst zulässt, dass der Ball
den unteren Rand seines Bildschirms berührt. Wenn der Ball den oberen Rand des Bildschirms berührt, soll er am oberen Rand
des Gegenspielers erscheinen und sich Richtung unterer Rand bewegen.

# Aufgaben
<hr>

Um die Umsetzung einfacher zu gestalten haben wir das Spiel in Meilensteine unterteilt. Jeder Meilenstein baut auf dem davor auf.
Mit der Erledigung jeder Teilaufgabe kommt ihr dem fertigen Pong Spiel einen Schritt näher. 

Nicht zu vergessen ist, dass wenn ihr Fragen habt oder nicht mehr weiterkommt: sprecht uns einfach an und wir helfen euch.
Fragen sind gern gesehen und tragen zum Verständnis bei.

Also, fangen wir an!

## Aufgabe 1

Ziel der ersten Aufgabe ist das Anzeigen des Spielballs und eines Spielerbalkens, ohne dass sich eines der beiden bewegen kann.
Das ist eine relativ leichte Aufgabe. Nutzt hier die Zeit auch dafür, um euch mit der Online Entwicklungsumgebung vertraut zu machen.
Welche Bausteine gibt es überhaupt? Wie funktioniert das zusammensetzen zu ersten Programmen? Welche Bausteine brauche ich?

[GIF TEILAUFGABE 1]

## Aufgabe 2

In der zweiten Aufgabe geht es darum, den Spielbalken zu programmieren. Wenn ihr also den A-Kopf drückt, soll der Balken
um eins nach links verschoben und beim Drückten des B-Kopfs um eins nach rechts verschoben werden. Denk auch daran, dass
der Balken nicht verschwinden soll, wenn ihr ihn zu oft nach rechts oder links verschiebt.

Ein Tipp zu Beginn: die Position des Balkens müsst ihr euch in einer Variable wie `balken_x` abspeichern.

[GIF TEILAUFGABE 2]

## Aufgabe 3

Hier geht es darum, dass der Ball automatisch anfängt, sich in eine bestimmte Richtung zu bewegen.
Die Richtungsänderung solltet ihr in den beiden Variablen `änderung_x` und `änderung_y` speichern, da sich der Ball ja
nicht nur horizontal oder vertikal bewegen soll, sondern diagonal. Außerdem wird die aktuelle Position des Balls mit den
Variablen `ball_x` und `ball_y` bestimmt. In der Aufgabe ist es noch nicht wichtig, dass ihr
das Verlieren oder Gewinnen des Spiels umsetzt. Baut das Spiel so, dass der Ball, wenn er eine der Kanten des
Bildschirms berührt die Richtung ändert, in die er sich bewegt. Das 'Gewinnen' und 'Verlieren' des Spiels bauen wir
in den nächsten Aufgaben ein.

[GIF TEILAUFGABE 3]

## Aufgabe 4

Der Ball und der Spielerbalken sollen miteinander interagieren! Wenn der Ball den Spielerbalken berührt, soll er die Richtung
ändern in die er sich bewegt.

[GIF TEILAUFGABE4]

## Aufgabe 5

Wir sind schon richtig weit gekommen! Nun geht es darum eine eigenständige Version des Spiels zu erstellen, die ohne einen
Mitspieler gespielt werden kann. Dazu sollt ihr das Spiel so umbauen, dass wenn der Ball die untere Kante des Bildschirms
berührt, ein trauriges Gesicht auf dem Bildschirm erscheint (Spiel verloren). Ihr könnt gerne auch etwas anzeigen lassen 
und herumexperimentieren.

Wieder ein Tipp zu Beginn: versucht eine Variable namens `status` einzufügen.

Bei `status = 0` befindet sich das Spiel am Anfang und wartet, bis der Spieler den B-Knop drückt, um das Spiel zu beginnen.

Bei `status = 1` hat das Spiel begonnen und läuft. Der Ball fängt an sich automatisch zu bewegen und der Spieler kann 
den Balken nach rechts und links bewegen.

Bei `status = 2` ist das Spiel verloren und das traurige Gesicht oder etwas anderes kann angezeigt werden.

[GIF AUFGABE 5]

## Aufgabe 6

In dieser Aufgabe kommt ein zweiter Calliope hinzu. Beim Starten beider Calliope soll der eine dem anderen eine Zahl senden.
Der jeweils andere soll darauf reagieren und auf dem Bildschirm etwas anzeigen.

Tipps bei dieser Aufgabe:
- schaut euch die Bausteine im Abschnitt 'Funk' in der online Entwicklungsumgebung an. Diese Bausteine beschäftigen sich mit der Datenübertragung zwischen mehreren Calliopes
- damit beide Calliope miteinander kommunizieren können, müssen sie in der gleichen Funkgruppe sein.

[GIF AUFGABE 6]

## Aufgabe 7

Super! Ihr wisst jetzt, wie zwei Calliope miteinander kommunizieren und Daten austauschen können. Als Nächstes sorgt dafür,
dass die Position des Balls beim Berühren der oberen Bildschirmkante an den anderen Calliope übertragen wird.

Auch hier wieder einige Tipps und Fragen, die euch weiterbringen, da diese Aufgabe eine der kniffligsten von allen ist:
- Die aktuelle Postion des Balls wird mit den Variablen `ball_x` und `ball_y` bestimmt. Die Richtung, in die sich der Ball bewegt wird durch die Variablen `änderung_x` und `änderung_y` bestimmt. Denkt darüber nach welchen Baustein ihr im Abschnitt 'Funk' in der Entwicklungsumgebung nutzen könnt, um zwei Werte <u>gleichzeitig</u> zu versenden. Ihr müsst auch nur zwei versenden. Denkt darüber nach welche zwei Werte versendet werden müssen, wenn der Ball oben beim gegnerischen Spieler erscheint und sich nach unten bewegen soll.
- Wie kann man eine Zahl in einen Text umwandeln, um möglicherweise zwei Wertepaare über Funk zu übertragen? Vielleicht findet man im Abschnitt 'Text' ja etwas Interessantes?
- Was soll mit dem Ball auf meinem Bildschirm passieren, wenn er auf dem Bildschirm meines Gegners auftaucht? Der Ball kann ja nicht doppelt angezeigt werden.

Hier soll das Spiel (noch als Zwischenschritt) so funktionieren, dass wenn der Ball die untere Kante eines der
Bildschirme berührt, beide Mitspieler verlieren und das traurige Gesicht auf beiden Bildschirmen angezeigt wird.

[GIF AUFGABE 7]

## Aufgabe 8 - Finale

Das Spiel ist schon fast fertig! Es fehlt nur noch, dass man tatsächlich gewinnt, wenn der Ball die untere Kante des
Gegners berührt und auf dem eigenen Bildschirm ein Smiley erscheint.

[GIF AUFGABE 8]
