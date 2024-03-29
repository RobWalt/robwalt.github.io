+++
title = "DKS Gymnasium Dresden (2023/2024) Updated: 23.10."
date = 2023-10-23
draft = false
[taxonomies]
tags=["voluntary", "school", "teaching"]
[extra]
toc=true
+++

# 1. Basics 

## GTA Programmieren 

In diesem Jahr wollen wir noch einmal ordentlich und strukturiert das Framework `p5.js` kennenlernen und mithilfe davon das Programmieren allgemein erlernen. Danach sollte der Weg geebnet sein um weiter spezieller Seiten der Programmierung zu erlernen. Darunter zaehlen unter anderem aber nicht ausschliesslich:

- Web-Entwicklung
- Spiele-Programmierung
- IT-Security ("Hacken")
- Entwicklung von Apps/Programmen
- Server-Entwicklung

## Das Framework `p5.js`

Wir werden hauptsaechlich in JavaScript programmieren. Dies ist "die Programmiersprache des Internets". Programme in JavaScript werden in Browsern ausgefuehrt. Zusaetzlich nutzen wir `p5.js`, ein JavaScript-Framework. Das bedeutet, dass wir zu den standardmaessig in JavaScript vorhandenen Grundbausteinen auch noch ein paar vorgefertigte Features erhalten, die uns das Leben einfacher machen werden.

## Was ist Programmieren?

Sehr einfach formuliert ist Programmieren das aufschreiben von Befehlen, die der Computer dann fuer uns in einem unglaublich schnellen Tempo ausfuehrt, wenn wir das Programm auf ihm starten. Um genau diese einfachen Befehle soll es in diesem ersten Kapitel gehen.

## Einfache `p5.js` Befehle

Zunaechst oeffnen wir einmal den `p5.js`-Editor, der ueber diese URL hier im Browser zu finden ist:

https://editor.p5js.org/

Wir sehen, dass bereits ein Grundgeruest an code fuer uns existert.

```js 
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}
```

Wenn wir das Programm ausfuehren, dann sehen wir folgendes Bild 

![Grauer Hintergrund beim Ausfuehren von p5js Standardprogramm](./imgs/001-basic.png)

Fuer das erste Kapitel reicht es aus, den Code wiefolgt anzupassen

```js 
function setup() {
  createCanvas(400, 400);
  background(220);
}
```

Das Ergebnis beim Ausfuehren sollte das Gleiche sein. Nun zur Erklaerung. Wie bereits gesagt, fuehrt der Computer einfach nur die Befehle aus, die wir ihm aufschreiben. Im Fall unserers ersten Programms hier sind das die folgenden zwei Befehle:

1. `createCanvas(400, 400);` -> dieser Befehl erstellt eine Art "Leinwand" auf die wir zeichnen koennen
2. `background(220);` -> dieser Befehl fuellt die Leinwand mit der grauen Farbe, die wir im Screenshot oben sehen koennen

Auf die Zahlen werden wir spaeter naeher eingehen. Ausserdem besteht unser Programm noch aus einer anderen Komponente:

```js 
function setup() {
  // hier steht der Rest
}
```

Das ist die sogenannte `setup` Funktion. Sie sagt dem Computer, dass er **einmalig** am Anfang des Programms alle Befehle ausfuehren soll, die zwischen den geschweiften Klammern (`{ ... }`) stehen. Damit haben wir eigentlich auch schon alles aus unserem ersten kleinen Programm erklaert.

> Nun moechte ich dir gerne ein paar neue Befehle zeigen und dich dazu einladen, damit herumzuexperimentieren. Bitte beachte, dass die neuen Befehle nach alle unter den `background(220);` Befehl gesetzt werden muessen und ansonsten nicht funktionieren werden!
>
> 1. Hier ist die Liste der Befehle. Anstatt von "ZAHL" kannst du einfach wirklich eine Zahl (z.B. 100) einsetzen:
>   - `ellipse(Zahl, Zahl, Zahl);`
>   - `rect(Zahl, Zahl, Zahl, Zahl);`
>   - `fill(Zahl);`
>   - `fill(Zahl, Zahl, Zahl);`
> 
> 2. Welchen Nutzen haben die einzelnen Zahlen? Was bewirken sie?
> 3. Hast du auch schon einmal probiert die Zahlen im `createCanvas` und `background` Befehl zu aendern? Was passiert, wenn du es tust?

## Die `p5.js` Reference

Es ist natuerlich etwas aufwendig jedes mal durch herumprobieren herauszufinden, welchen Nutzen die Zahlen der Befehle haben. Dafuer gibt es eine Art kleine Suchmaschine nur fuer die `p5.js` Befehle. Du kannst sie unter folgender URL finden:

https://p5js.org/reference/

Hier sind alle Befehle gelistet, die mit `p5.js` "mitgeliefert" werden. Dazu gibt es immer 

- eine Beschreibung, was der Befehl macht
- ein Beispiel
- ganz unten die Erklaerung der Zahlen

> Haben deine Vermutungen beim experimentieren von gerade eben gestimmt? Hier kannst du es ueberpruefen, indem du die Befehle suchst

Du kannst auch sehen, dass einige der Befehle von oben (wie `fill`) unterschiedlich viele Zahlen nehmen koennen. Hier kannst du alle Moeglichkeiten herausfinden.

Unter der Ueberschrift `Shape -> 2D Primitives` kannst du uebrigens noch weitere Befehle zum einfachen zeichnen finden.

> Probiere dich gerne noch weiter aus. Wie viele der existierenden Zeichenbefehle bekommst du zum Laufen? Was tun sie?

## Beispiel Programm Kapitel 1

Da ich denke, dass es manchmal nuetzlich ist anhand von Beispielen zu lernen liefere ich jede Woche auch ein Beispiel mit. 

### Hier ist das Beispiel dieser Woche

```js  
function setup() {
  createCanvas(400, 400);
  background(220);
  
  fill(240, 40, 40)
  rect(100, 100, 100, 100)

  fill(220, 60, 60)
  rect(110, 110, 100, 100)

  fill(200, 80, 80)
  rect(120, 120, 100, 100)

  fill(180, 100, 100)
  rect(130, 130, 100, 100)

  fill(160, 120, 120)
  rect(140, 140, 100, 100)

  fill(140, 140, 140)
  rect(150, 150, 100, 100)

  fill(120, 160, 160)
  rect(160, 160, 100, 100)

  fill(100, 180, 180)
  rect(170, 170, 100, 100)

  fill(80, 200, 200)
  rect(180, 180, 100, 100)

  fill(60, 220, 220)
  rect(190, 190, 100, 100)

  fill(40, 240, 240)
  rect(200, 200, 100, 100)
}
```

![Overlapping rectangles which have colors ranging from red smoothly to a sky blue](./imgs/002-example1.png)

# 2. Loops und neue Befehle

## Hilfreiche Werte (`width`, `height`)

Zunaechst einmal werden wir ein paar weitere hilfreiche Werte kennenlernen. In unseren letzten Programmen war es teilweise schwierig die Formen perfekt auszurichten. Dafuer koennen wir die Werte `width` und `height` nutzen. Diese speichern:

- in `width` die Breite von der Leinwand, der erste Wert in den Klammern bei `createCanvas(200, 400)`, also hier hat `width` den Wert `200`
- in `height` die Hoehe von der Leinwand, der zweite Wert in den Klammern bei `createCanvas(200, 400)`, also hier hat `height` den Wert `400`

Wenn wir zum Beispiel einen Kreis in der Mitte der Leinwand malen wollen, koennen wir einfach den Punkt nehmen, der jeweils genau auf der Haelfte der Breite und der Hoehe liegt, also

```js 
function setup() {
  createCanvas(400, 400)
  background(200)
  circle(width / 2, height / 2, 100)
}
```

Auch wenn du die Werte im `createCanvas` Befehl aenderst, wird nun der Kreis immer perfekt in der Mitte platziert werden.

![A white circle that is centered on a square canvas](./imgs/003-centered.png)

## Zufaellige Zahlenwerte (`random`)

Als naechstes lernen wir einen neuen Befehl kennen, mit dem wir viel Variation in unsere Programme bekommen koennen. Der Befehl heisst `random` und kann auf folgende Arten und Weisen verwendet werden: 

- `random()`, generiert eine zufaellige Zahl zwischen `0.0` und `1.0`
- `random(min, max)`, hier muss man fuer `min` und `max` Zahlen einsetzen, dann generiert der Befehl eine zufaellige Zahl zwischen `min` und `max`

Das koennen wir nun zum Beispiel verwenden um einen Kreis an einer zufaelligen Position zu zeichnen: 

```js 
function setup() {
  createCanvas(400, 400)
  background(200)
  circle(random(0, width), random(0, height), 100)
}
```

Der Mittelpunkt des Kreises hat einen x-Wert zwischen 0 und der maximalen Breite der Leinwand und einen y-Wert zwischen 0 und der maximalen Hoehe der Leinwand. Jedes Ausfuehren des Programms wird einen Kreis an einer neuen Position zeichnen. Ausserdem koennen wir auch die Farbe des Kreises zufaellig Waehlen, wenn wir noch den `fill` Befehl in Kombination mit `random` nutzen.

```js 
function setup() {
  createCanvas(400, 400)
  background(200)
  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)
}
```

Nicht vergessen, die RGB Werte haben fuer jede Farbe (Rot, Gruen, Blau) einen Zahlenwert zwischen 0 und 255. Dementsprechend haben wir auch das `min` und das `max` von `random` gewaehlt.

## For-Schleifen (For Loops)

Nun koennen wir schoene kuenstleriche Meisterwerke generieren, indem wir einfach ganz viele zufaellige Kreise mit zufaelligen Farben vom Computer auf die Leinwand zeichnen lassen:

```js 
function setup() {
  createCanvas(400, 400)
  background(200)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)

  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)
}
```

Wie man aber sehen kann ist es sehr muehselig so viel dafuer zu schreiben. Noch schlimmer ist, dass wenn wir jetzt die Groesse der Kreise auch noch zufaellig waehlen wollen, wir in jeder Zeile die `100` durch `random(0, 100)` (oder sowas in der Art) ersetzen muessen. Das kann ganz schoen nervig werden! Dafuer gibt es aber auch Hilfsmittel: Die sogenannten For-Schleifen. Lasst uns sie erst einmal ausprobieren, bevor wir uns im Detail anschauen, wie sie funktionieren:

```js 
function setup() {
  createCanvas(400, 400)
  background(200)

  for (let i = 0; i < 10; i=i+1) {
    fill(random(0, 255), random(0, 255), random(0, 255))
    circle(random(0, width), random(0, height), 100)
  }
}
``` 

Dieser Code macht das selbe wie der letzte Code und ist viel kuerzer durch die For-Schleifen. Wir koennen schon grob sehen, dass wir alles was zwischen den geschwungenen Klammern `{` und `}` schreiben 10 mal ausgefuehrt wird, da wir sowas wie `i < 10` geschrieben haben. Aber wie funktioniert das jetzt eigentlich?

- Zunaechst beginnt jede For-Schleife mit dem Wort `for` (wovon sie auch ihren Namen hat). Das ist hauptsaechlich dazu da, damit der Computer ab dieser Stelle weiss "Aha, jetzt interpretiere ich erstmal alles was folgt als eine For-Schleife". Es signalisiert ihm also das jetzt etwas besonderes kommt.
- Darauf folgen Runde Klammern, die immer wiefolgt aufgebaut sind: `( START_BEFEHL, CHECK_OB_ENDE_ERREICHT, SCHRITT_BEFEHL )`. Hier eine naehere Erklaerung der einzelnen Komponenten
  - `START_BEFEHL` wird einmal am Anfang der For-Schleife ausgefuehrt, bevor die erste Runde der Schleife loslaeuft. In unserem Fall legen wir eine Variable an, die wir fuer das Zaehlen verwenden `let i = 0`. `i` kann interpretiert werden als: "Wir haben die Schleife schon i-Mal ausgefuehrt"
  - mit `CHECK_OB_ENDE_ERREICHT` wird ueberprueft, ob wir die Schleife nocheinmal ausfuehren sollen oder ob wir fertig sind. In unserem Fall checken wir, ob unsere Variable einen gewuenschten Wert erreicht hat `i < 10`. Man kann das lesen als: "Solange i noch kleiner 10 ist, fuehre nochmal die Schleife aus". Wenn `i = 10` (oder `i > 10`), dann bricht die Schleife in unserem Fall ab.
  - `SCHRITT_BEFEHL` wird jedes Mal ausgefuehrt, wenn die Schleife einmal durchgelaufen ist. In unserem Fall zaehlen wir einfach die Variable um eins nach oben `i = i+1`. Das kann gelesen werden als: "Nimm den alten Wert von i, addiere 1 und dann speichere es wieder in die Variable i ab"
- Zuletzt kommen hinter den runden Klammern noch geschwungene Klammern und zwischen diesen geschwungenen Klammern kommen alle Befehle, die wir wiederholt ausfuehren wollen

Lasst uns nocheinmal das Beispiel von oben Schritt fuer Schritt durchgehen:

```js 
for (let i = 0; i < 10; i=i+1) {
  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)
}
```

1. Der Computer entdeckt die For-Schleife
2. Der `START_BEFEHL` wird ausgefuehrt (`let i = 0`)
3. Nun wird der `CHECK_OB_ENDE_ERREICHT` gemacht: `i < 10` ? Wir setzen ein : `0 < 10`. Das stimmt, also brechen wir noch nicht ab
4. Nun wird die Schleife das erste Mal ausgefuehrt also der erste bunte Kreis wird gemalt mit
  ```js 
  fill(random(0, 255), random(0, 255), random(0, 255))
  circle(random(0, width), random(0, height), 100)
  ```
5. Wenn die Befehle in der Schleife durchgelaufen sind, wird `SCHRITT_BEFEHL` ausgefuehrt: `i = i+1`, also eingesetzt steht da `i = 0 + 1` also ist nun `i = 1`
6. Nun wird wieder der `CHECK_OB_ENDE_ERREICHT` gemacht: `i < 10` ? Wir setzen ein : `1 < 10`. Das stimmt, also brechen wir immer noch nicht ab
7. Nun wird die Schleife das erste Mal ausgefuehrt also der zweite bunte Kreis wird gemalt mit
8. Wenn die Befehle in der Schleife durchgelaufen sind, wird `SCHRITT_BEFEHL` wieder ausgefuehrt: `i = i+1`, also eingesetzt steht da `i = 1 + 1` also ist nun `i = 2`
...
9. Das wird immer weiter wiederholt bis irgendwann `i = 10` ist
10. Dann wird wieder der `CHECK_OB_ENDE_ERREICHT` gemacht: `i < 10` ? Wir setzen ein : `10 < 10`. Das stimmt nicht mehr, also brechen wir ab

Man kann die Variable `i` uebrigens auch in der Schleife in die Befehle einbauen. Zum Beispiel in 

```js 
for (let i = 0; i < width; i = i + 25) {
  fill(random(0, 255), random(0, 255), random(0, 255));
  circle(i, height / 2, i / 10);
}
```

Wird alle 25 Pixel zwischen 0 und `width` ein Kreis mit einem Mittelpunkt mit x-Wert i (0, 25, 50, 75, 100, ...), auf mittiger Hoehe und einem Radius von `i / 10` (0, 2.5, 5.0, 7.5, 10.0, ...) gezeichnet.

![Circles with random colors in a line growing bigger from left to right](./imgs/004-loops.png)

## Die `draw` Funktion, `frameRate` und `frameCount`

Neben der `setup` Funktion, die wir bis hierher verwendet haben und die einmal am Anfang des Programs ausgefuehrt wird, existiert auch noch eine andere Funktion. Die `draw` Funktion sieht bis auf ihren Namen genauso aus wie die setup Funktion

```js 
function draw() {
}
```

Der Unterschied zwischen den beiden Funktionen ist, dass die `draw` Funktion im Gegensatz zu `setup` wiederholt mit einer sogenannten "frame rate" ausgefuehrt wird. Die frame rate koennen wir in der `setup` Funktion mit `frameRate(ZAHL)` festlegen und sie gibt an, wie oft die `draw` Funktion jede Sekunde ausgefuehrt werden soll.

```js 
function setup() {
  createCanvas(400, 400)
  frameRate(2)
}

function draw() {
  background(200)
  fill(random(0, 255), random(0, 255), random(0, 255));
  circle(width / 2, height / 2, 100);
}
```

Dieses Programm, malt zwei mal in der Sekunde einen Kreis mit einer neuen Farbe mittig auf die Leinwand. Neben dem `frameRate` Befehl gibt es auch noch den `frameCount` Wert. Dieser gibt uns an, wie oft `draw` schon ausgefuehrt wurde und zaehlt jedes Mal um eins hoch, wenn die letzte Zeile in `draw` ausgefuehrt wurde.

```js 
function setup() {
  createCanvas(400, 400)
  frameRate(30)
}

function draw() {
  background(200)
  circle(frameCount, height / 2, 100);
}
```

In diesem Beispielprogramm hat der Kreis immer einen x-Wert vom aktuellen `frameCount` Wert. Dieser startet bei 0, also startet der Kreis am linken Rand. Da der `frameCount` langsam steigt, "bewegt" sich der Kreis langsam nach rechts.

<!-- ## Noise

Bisher haben wir schon zufaellige Zahlen kennengelernt. Diese sind aber nicht wirklich hilfreich, wenn wir sie in der `draw` Funktion mit hoher `frameRate` verwenden wollen. Im folgenden Programm sehen wir zum Beispiel nur wildes rumgeflacker, da die Werte schon fast zu zufaellig gewaehlt werden

```js 
function setup() {
  createCanvas(400, 400)
  frameRate(30)
}

function draw() {
  background(200)
  circle(random(0, width), random(0, height), 100);
}
```

Wir malen 30 mal in der Sekunde irgendwo an einer zufaelligen Stelle einen Kreis. Um die Aenderungen ein bisschen sanfter zu gestalten, gibt es eine zweite Form von zufaelligen Zahlen. Diese koennen wir mit dem `noise(ZAHL)` Befehl erzeugen. Im Gegensatz zu `random` koennen wir bei `noise` keine Maximum und Minimum Werte angeben. Die Zahl, die `noise` erzeugt liegt immer zwischen 0.0 und 1.0. Da stellt sich dann trotzdem die Frage: Warum muessen wir dem Befehl eine Zahl als Eingabe uebergeben? Die Zahl wird genutzt, um die zufaellige Zahl zu erzeugen. 
-->

# 3. Maus, Variablen und Listen

## Maus - Werte

Zunaechst gibt es, wie schon in all unseren anderen Wochen, ein paar neue nuetzliche Werte, die uns helfen ganz einfach coole Programme zu schreiben. Dieses mal schauen wir uns `mouseX` und `mouseY` an. Wie die Namen schon halb verraten, sind das die X-und-Y-Werte der Maus. Diese werden dauernd geupdated sodass der Wert immer die wirkliche aktuelle Position des Mauszeigers darstellt. Man kann die Werte ganz einfach nutzen:

```js 
function setup() {
  createCanvas(400, 400)
  background(200)
}

function draw() {
  background(200)
  circle(mouseX, mouseY, 100);
}
```

In diesem Program wird jede Sekunde der Bildschirm mit der Hintergrundfarbe uebermalt und dann ein Kreis an der aktuellen Position des Mauszeigers gemalt.

![A white circle is painted and follows the cursor](./imgs/005-mousexy.gif) 

Man kann die Werte auch fuer andere Sachen als nur die Position benutzen. Versuche einmal selbst folgendes:

1. Verwende den Wert `mouseX` um die Groesse eines Kreises zu steuern, der in der Mitte von der Leinwand ist 
2. Verwende beide Werte `mouseX` und `mouseY` um die Farbe eines Kreises zu steuern. Was passiert, wenn du die Werte unterschiedlich kombinierst?
  - `mouseX + mouseY`
  - `mouseX - mouseY`
  - `mouseX * mouseY`

## Listen und Variablen

Da heute die Idee aufkam etwas zu machen, was in Richtung eines "SNAKE" Spiels geht, haben wir uns ein dafuer wichtiges Konzept angeschaut. Das ist das Konzept der Listen.

Listen im Computer verhalten sich ganz aehlich wie Listen in der richtigen Welt: Wir nutzen sie um eine Ansammlung von Dingen zu speichern. In JavaScript koennen wir eine Liste wiefolgt erstellen:

```js 
let liste = [50, 40, 30, 20, 10]
```

Das `let` Wort kennen wir schon aus den For-Schleifen. Es sagt dem Computer einfach, dass das was folgt eine Variable ist. Mithilfe von Variablen koennen wir Dinge abspeichern waehrend unser Programm laeuft. In diesem Fall speichern wir etwas unter dem Variablen-Namen `liste`. Du kannst dir hier aber auch jeden beliebigen Namen waehlen (`listeABC`, `merkzettel`, `quark`, ...) solange der Name nur Buchstaben enthaelt. Der Wert der Variable steht dann auf der anderen Seite von dem `=`. Die eckigen Klammern `[` und `]` deuten dem Computer an, dass wir eine Liste speichern. In der Liste koennen wir dann Zahlenwerte mit Komma getrennt speichern. Oh man ... das war jetzt viel Text 🥱

Lasst uns also mal schauen wie wir die Liste nun verwenden koennen. Mein Programm sieht jetzt so aus

```js 
let liste = [50, 40, 30, 20, 10]

function setup() {
  createCanvas(400, 400)
  background(200)
}
```

Wenn wir das ausfuehren passiert erstmal nix. Die Werte werden ja noch nicht verwendet. Um auf einen Wert in der Liste zuzugreifen, koennen wir folgendes schreiben:

```js 
let liste = [50, 40, 30, 20, 10]

function setup() {
  createCanvas(400, 400)
  background(200)
  circle(100, 100, liste[0])
}
```

Hier nutzen wir also `liste[0]`. Das heisst soviel wie: Nutze den 0-ten Wert in der Liste. Der Computer schaut dann fuer uns diesen Wert nach und setzt ihn dort ein. Der Code oben ist also der gleiche wie

```js 
let liste = [50, 40, 30, 20, 10]

function setup() {
  createCanvas(400, 400)
  background(200)
  circle(100, 100, 50)
}
```

da `50` das 0-te Element in der Liste ist. In der Informatik faengt man uebrigens bei 0 an zu zaehlen, was ziemlich verwirrend sein kann. Fragt mich lieber nicht wieso 🫣 Achtung: Das erste Element ist immer an Stelle 0, das zweite Element ist immer an Stelle 1 und so weiter 😵‍💫. Wenn wir nun die ganze Liste (also alle Werte in der Liste) verwenden wollen koennen wir also schreiben

```js 
let liste = [50, 40, 30, 20, 10]

function setup() {
  createCanvas(400, 400)
  background(200)
  circle(100, 100, liste[0])
  circle(100, 100, liste[1])
  circle(100, 100, liste[2])
  circle(100, 100, liste[3])
  circle(100, 100, liste[4])
}
```

![Multiple overlapping circles with radii from a list](./imgs/006-list.png) 

Wie zu sehen ist, muessen wir uns ziemlich oft wiederholen, um alle Werte aus der Liste zu nutzen. Was koennte uns mit Wiederholungen helfen? Richtig: For-Schleifen. Es gibt eine Standard-Loesung um etwas mit allen Werten in einer Liste zu machen, die wiefolgt aussieht:

```js 
let liste = [50, 40, 30, 20, 10]

function setup() {
  createCanvas(400, 400)
  background(200)
  for (let i = 0; i < liste.length; i++) {
    circle(100, 100, liste[i])
  }
}
```

![Multiple overlapping circles with radii from a list](./imgs/006-list.png) 

Das macht genau dasselbe wie das letzte Programm. `liste.length` ist wie der Name schon sagt die Laenge der Liste, also in unserem Fall hier 5. Im ersten Durchlauf der Schleife fuehren wir den Befehl mit dem ersten Element (Achtung Element an Stelle 0!) aus. In der zweiten Wiederholung der Schleife ist das zweite Element dran und so weiter. Das coole nun ist: Wenn wir neue Elemente in die Liste schreiben, brauchen wir nun nicht mehr eine neue Zeile wie 

```js 
    circle(100, 100, liste[5])
```

schreiben, sondern die For-Schleife "merkt" automatisch, dass das neue Element da ist und malt es auch.

```js 
let liste = [100, 90, 80, 70, 60, 50, 40, 30, 20, 10]

function setup() {
  createCanvas(400, 400)
  background(200)
  for (let i = 0; i < liste.length; i++) {
    circle(100, 100, liste[i])
  }
}
```

![Even more overlapping circles with radii from a list](./imgs/007-listbig.png) 

Zum Schluss koennen wir noch einen ersten Prototypen von unserem "SNAKE" Spiel bauen. Dazu nutzen wir auch eine Liste und speichern darin die x-Werte der einzelnen SNAKE-Kreise.

```js 
let snake_liste = [0, 0, 0, 0, 0]

function setup() {
  createCanvas(400, 400)
  frameRate(3)
}

function draw() {
  background(200)
  snake_liste[4] = snake_liste[3]
  snake_liste[3] = snake_liste[2]
  snake_liste[2] = snake_liste[1]
  snake_liste[1] = snake_liste[0]
  snake_liste[0] = frameCount * 10

  for (let i = 0; i < snake_liste.length; i++) {
    circle(snake_liste[i], 200, 10)
  }
}
```

🐍🎉

Der einzig richtig neue Code hier ist 

```js 
  snake_liste[4] = snake_liste[3]
  snake_liste[3] = snake_liste[2]
  snake_liste[2] = snake_liste[1]
  snake_liste[1] = snake_liste[0]
  snake_liste[0] = frameCount * 10
```

Das bedeutet so viel wie: 

- nimm den Wert an Stelle 3 und schieb ihn an Stelle 4
- nimm den Wert an Stelle 2 und schieb ihn an Stelle 3
- nimm den Wert an Stelle 1 und schieb ihn an Stelle 2
- nimm den Wert an Stelle 0 und schieb ihn an Stelle 1
- Speichere den neuen Wert `frameCount * 10` an Stelle 0

Damit ruecken die Kreise Stueck fuer Stueck nach. An Stelle 0 kommen immer neue Werte in die Liste (das ist also der Kopf) und den alten Wert von Stelle 4 ueberschreiben wir komplett (wir werfen ihn quasi weg, das ist das andere Ende der Schlange)

Expertenaufgabe: Vielleicht ist es der ein oder anderen Person schon aufgefallen. Beim "Nachruecken" wiederholt sich wieder viel Code. Was kann man also anwenden? Unsere gute Freunding die For-Schleifen! Du kannst ja mal versuchen das umzusetzen, wenn du magst. Ich gebe das grobe Geruest vor:

```js 
let snake_liste = [0, 0, 0, 0, 0]

function setup() {
  createCanvas(400, 400)
  frameRate(3)
}

function draw() {
  background(200)

  for (let i = snake_liste.length; i > 0; i--) {
    // ???
  }

  snake_liste[0] = frameCount * 10

  for (let i = 0; i < snake_liste.length; i++) {
    circle(snake_liste[i], 200, 10)
  }
}
```

Wie du sehen kannst, koennen wir auch von der anderen Seite Schleifen verwenden: Wir fangen beim oberen Grenzwert an und Zaehlen runter bis zur 0 (mit `i--`, das heisst "zieh eins ab").

# 4. Zurueck zum Anfang mit Rust

Aufgrund von neuen technischen Begebenheiten (Laptops) haben wir nun mehr Freiheiten und sind nicht mehr auf p5.js zum Programmieren angewiesen. Die neue Idee ist deshalb nun nocheinmal von ganz vorn und in der Programmiersprache Rust durchzustarten. Trotzdem werden sich die Dinge, die wir bis hierher gelernt haben als nuetzlich ueberweisen und uebertragen lassen.

## Die Programmierumgebung

Ich habe soweit alles vorbereitet, sodass keine grossartigen setups noetig sind, um loszustarten. Auf den Laptops ist die Linuxvariante [NixOS](https://nixos.org/download.html) bereits im Vorfeld von mir installiert worden. Das ermoeglicht es mir "Bau-Anleitungen" fuer die Programmierumgebungen zu schreiben, die dann mit nur einem Befehl automatisch alles einrichten.

Die Anleitung, die wir als erstes nutzen wird wiefolgt ausgefuehrt:

```nix
nix develop github:RobWalt/HEG-GTA#comfyNew
```

Wenn der Befehl durchgelaufen ist, sollte sich VSCode mit einem Beispiel-Platzhalter-Projekt oeffnen.

![VSCode is open after executing the nix command](./imgs/008-vscode.png) 

VSCode braucht ein bisschen Zeit, um die Dateien zu analysieren. Wenn das geschafft ist, dann kannst du das Beispiel Programm ausfuehren, indem du in der `main.rs` Datei auf `Run` klickst. 

![Run button is highlighted](./imgs/009-run.png) 

Danach sollte folgendes zu sehen sein.

![A bluish square on a black background](./imgs/010-basicrust.png) 

## Selbst das Programm anpassen - Variablen anlegen in Rust

Als erstes wollen wir etwas sehr einfaches machen, was wir schon in p5 kennengelernt haben: Eine Variable anlegen. Dazu oeffnen wir zunaechst die `lib.rs` Datei. Das ist die Datei in der wir hauptsaechlich arbeiten werden, wenn wir selbst programmieren. Sie sieht erstmal wiefolgt aus 

```rust 
pub mod boilerplate;
pub use boilerplate::*;
use comfy::*;

#[derive(Default)]
pub struct GameState {}

pub fn setup(_c: &mut GameContext) {}

pub fn update(c: &mut GameContext) {
    let GameState {} = &mut c.state;
    draw_rect(Vec2::ZERO, Vec2::ONE, Color::rgb(0.0, 0.1, 0.2), 0);
}
```

Hier macht es zum Beispiel Sinn eine Variable mit dem Namen `center` fuer die Mitte des Rechtecks anzulegen und zu nutzen. Das koennte dann wiefolgt funktionieren. Wir passen dafuer die Funktion `update` an.

```rust
pub fn update(c: &mut GameContext) {
    let GameState {} = &mut c.state;

    let center = Vec2::new(0.0, 0.0); // neu

    draw_rect(center, Vec2::ONE, Color::rgb(0.0, 0.1, 0.2), 0);
    //        ^^^^^^ neu
}
```

Im Gegensatz zu p5.js nutzen wir nicht zwei einzelne Zahlenwerte fuer `x` und `y`, sonder buendeln beide Werte in dem Positions-Typen `Vec2` zusammen. Nuetzlicherweise erwartet die `draw_rect` Funktion genau dieses Typen, um die Mitte des Rechtecks zu wissen. Wenn wir das Programm nun ausfuehren, werden wir sehen, dass sich nichts weiter geaendert hat. Die Variable dient momentan hauptsaechlich der besseren Lesbarkeit. Neben dieser Eigenschaft, bietet `Vec2` auch noch andere Vorteile, die wir im weiteren Verlauf kennenlernen werden.

Ganz allgemein, kann man sagen, dass das Anlegen von Variablen in Rust eigentlich mehr oder weniger genauso aussieht wie in JavaScript in p5. Es folgt dem Schema 

```rust 
let NAME = WERT;
```

Das einzige, was zu beachten ist, ist dass das Semikolon am Ende der Variablen-Definition wichtig ist. Rust ist jedoch so nett und weisst uns recht genau darauf hin, falls wir es vergessen.

## Nutzen von `GameState`

Momentan definieren wir noch die Variable `center` in der `update` Funktion. Das bedeutet, dass wir den Wert von `center` jedes frame neu auf einen konstanten Wert setzen. Damit gibt es leider keine Moeglichkeit fuer uns das `center`, also die Position, des Rechtecks zu veraendern ... Doch wartet! Es gibt einen Ausweg: Hier ist der Grund weshalb wir diesen komischen Code rund um `GameState` bereits im Programm haben. In `GameState` kann man Daten von Variablen ueber mehrere Frames speichern. Und hier ist, wie das geht:

```rust 
pub mod boilerplate;
pub use boilerplate::*;
use comfy::*;

#[derive(Default)]
pub struct GameState {
    // hier wird der Name und der Typ der Daten, die
    // wir speichern wollen im Format "Name: Typ" angegeben
    center: Vec2, 
}

pub fn setup(c: &mut GameContext) {
    //      ^^^ Unterstrich entfernt

    // Hier wird nun in der setup Funktion einmalig am 
    // Anfang vom Programm der Wert von center gesetzt
    c.state.center = Vec2::new(0.0, 0.0); // new
}

pub fn update(c: &mut GameContext) {
    let GameState { center } = &mut c.state;
    //             ^^^^^^^^ new
    
    // Die Variablen-Definition koennen wir hier jetzt wieder loeschen

    draw_rect(*center, Vec2::ONE, Color::rgb(0.0, 0.1, 0.2), 0);
    //       ^^^^^^^^^ new, bitte beachtet, dass man hier einen Stern davor machen muss!
}
```

Damit haben wir nun `center` nicht mehr als Variable, sondern als "Feld in unserem GameState struct". An und fuer sich, macht dieser Code jetzt immernoch das gleiche wie vorher. Nun koennen wir aber in `update` den Wert von `center` veraendern und damit das Rechteck bewegen.

```rust
pub fn update(c: &mut GameContext) {
    let GameState { center } = &mut c.state;

    // erhoehe den x Wert von center ein kleines bisschen, also 
    // bewege das Rechteck nach rechts
    center.x += 0.05;

    draw_rect(*center, Vec2::ONE, Color::rgb(0.0, 0.1, 0.2), 0);
}
```

Kleiner Check am Rande: Um zu ueberpruefen, dass ich hier keinen Mist erzaehle, empfehle ich mal nachzuschauen, was passiert wenn man den Wert von `center` genauso wie oben aendert, wenn `center` aber als Variable definiert ist. Also was passiert wirklich, wenn die `update` Funktion wiefolgt aussieht:

```rust
pub fn update(c: &mut GameContext) {
    let GameState { } = &mut c.state;

    let mut center = Vec2::new(0.0, 0.0);
    // ^^^^^ das muss man schreiben, damit man den Wert aendern darf
    center.x += 0.05;

    draw_rect(center, Vec2::ONE, Color::rgb(0.0, 0.1, 0.2), 0);
    //        ^^^^^^ Wenn center eine Variable ist, brauchen wir hier nicht den Stern
}
```

## Keyboard input

Nun wollen wir ein bisschen Interaktion in unser Programm bringen. Am besten waere, wenn wir bestimmte Dinge tun koennen, wenn wir bestimmte Tasten druecken. Dafuer gibt es sogenannte If-Bedingungen. Ich gebe mal ein zum Einstieg ein Beispiel:

```rust
pub fn update(c: &mut GameContext) {
    let GameState { center } = &mut c.state;

    if is_key_pressed(KeyCode::Up) {
        center.y += 0.05;
    }

    draw_rect(*center, Vec2::ONE, Color::rgb(0.0, 0.1, 0.2), 0);
}
```

Die If-Bedingungen beginnen immer mit dem Schluesselwort `if`. Darauf folgt etwas was entweder wahr oder falsch sein kann. In unserem Fall check wir, ob eine Taste gedrueckt ist oder nicht. Wenn die Bedingung dann wahr ist, wird der Code in den Klammern `{ ... }` ausgefuehrt. In unserem Fall heisst das: Das Rechteck bewegt sich nach oben, wenn wir die Pfeil-nach-oben-Taste gedrueckt halten.

## Uebungen

1. Implementiere die komplette Steuerung des Rechtecks in alle Richtungen (also auch noch fuer `KeyCode::Down, KeyCode::Left, KeyCode::Right`)
2. Fuege zum `GameState` noch ein neues Feld `speed` vom Typ `f32` (das sind Kommazahlen) hinzu und tausche es ueberall fuer den festen Wert `0.05` aus. Also:
    ```rust 
        if is_key_pressed(KeyCode::Up) {
            center.y += *speed;
        }
    ```
    Beachte, dass du hierbei das Sternchen auch wieder verwenden musst.
3. Implementiere etwas, womit man bei Tastendruck den `speed` veraendern kann. Achtung! Auch hier musst du IMMER `*speed` schreiben. 
4. Begrenze mit weiteren If-Bedingungen des `speed`, damit er nicht zu hoch wird. Also wenn `speed` groesser als eine obere Grenze oder kleiner als eine untere Grenze ist, dann setze den Wert nicht noch hoeher/tiefer, sondern setze ihn auf den Wert der Grenze.

# 5. Hinterteil der Schlange

Nun haben wir bereits den Kopf der Schlange implementiert. Das naechste logische Element ist es, den Rest des Koerpers der Schlange zu implementieren. Dazu werden wir Listen (auch Vektoren genannt) von Positionswerten verwenden. Deshalb jetzt erstmal ganz allgemein eine kleine Einfuehrung zu was Vektoren ueberhaupt sind und was man alles mit ihnen machen kann.

## Listen (Vektoren)

Zunaechst klaeren wir einmal ganz grundlegende Fragen 

### Wozu sind Listen nuetzlich?

Listen werden eingesetzt, um effektiv mehrere Daten von der gleichen Form (Typ), die aber unterschiedliche Werte haben, zu speichern. Nehmen wir folgendes Beispiel: Wir wollen eine Sammlung an Namen speichern. Dazu koennten wir nun mit unserem bisherigen Wissen einfach Variablen verwenden: 

```rust 
let name1 = "Hannelore";
let name2 = "Hans";
let name3 = "Marlene";
let name4 = "Dieter";
let name5 = "Berta";
```

Das wird nur leider sehr muehselig, umso mehr Namen es werden. Ausserdem ist es auch genauso aufwendig diese dann zu nutzen. Wollen wir sie zum Beispiel in der Konsole ausgeben, koennten wir schreiben:

```rust 
println!("Hallo, {name1}!");
println!("Hallo, {name2}!");
println!("Hallo, {name3}!");
println!("Hallo, {name4}!");
println!("Hallo, {name5}!");
...
```

Mit Listen ist das alles viel einfacher und wir ersparen uns die staendigen Wiederholungen:

```rust
let names = vec!["Hannelore", "Hans", "Marlene", "Dieter", "Berta"];

for name in names {
  println!("Hallo, {name}!");
}
```

Diese 5 Zeilen tun genau das, was die vorherigen 10 Zeilen machen. Wie zu sehen ist sparen wir uns also viel Code damit. Auch Aenderungen sind einfacher: Ein neuer Name bedeutet:

- ohne Listen: 2 neue Zeilen
- mit Listen: 1 neuer Eintrag (der Name) in der Liste

### Wie werden Listen erstellt?

Wie schon in den bisherigen Codeschnippseln zu sehen war werden Listen mit `vec![...]` erstellt, wobei `...` eine Aufreihung von Werten in der Liste sind. Diese Werte muessen vom selben Typ sein. Das heisst es ist nicht erlaubt z.B. Text und Zahlen zu mischen.

- erlaubt: `vec![1,2,3,4,5]`, `vec!["rot", "gelb", "blau"]`
- nicht erlaubt: `vec!["Sonne", 1.5, 0]`

### Was koennen Listen noch?

Es folgt noch eine kurze Liste von nuetzlichen Funktionen von Listen: 

- `.len()` gibt die Anzahl der Elemente in der Liste zurueck: `vec![1,2,3].len() == 3`
- `.get(index)` gibt das Element an der Stelle `index` nur mit Leserechten zurueck, sofern es existiert. Achtung! Wir beginnen bei 0 zu zaehlen: `vec![1,2,3].get(1) == 2`
- `.get_mut(index)` gibt das Element an der Stelle `index` mit Schreibrechten zurueck, sofern es existiert: 
  ```rust 
  let mut liste = vec![1,2,3];
  let zwei = liste.get_mut(1).unwrap();
  *zwei = 22;
  liste = vec![1,22,3];
  ```
- `.remove(index)` gibt auch das Element an der Stelle `index` zurueck und entfernt es gleichzeitig: 
  ```rust 
  let mut liste = vec![1,2,3];
  let zwei = liste.remove(1);
  liste == vec![1,3];
  ```
  alle Elemente nach dem entfernten Element "rutschen nach links nach"
- `.push(element)` haengt ein neues Element ans Ende der Liste
  ```rust 
  let mut liste = vec![1,2,3];
  liste.push(4);
  liste == vec![1,2,3,4];
  ```

## Hinterteil der Schlange mit Listen

Da das ein etwas umfangreicherer Teil unseres Programms ist, stellen wir erstmal einen Plan auf. Die Grundidee, um die einzelnen Teile des Restes der Schlange zu simulieren ist folgende: 

(Idee aus dem GTA heraus spontan entstanden. Danke Leute!)

1. die Position des Kopfes wird fuer x Schritte zu gespeichert (in einer Liste)
  - dazu legen wir eine Liste fuer die Positionen an 
  - wir fuegen jedes Frame die aktuelle Position des Kopfes hinten an die Liste an 
  - wenn die Liste groesser als eine vorher festgelegte Laenge ist, loeschen wir den ersten Eintrag sodass alle anderen Eintraege nachrutschen (siehe Erklaerung von `.remove(index)`)
2. die Position eines nicht-Kopf-Teils der Schlange wird auf eine der Positionen aus der Vergangenheit aus der Liste gesetzt
  - wir legen eine Anzahl an Teilen der Schlange fest 
  - wir legen eine Schrittgroesse fest, die sagt wie weit wir in die Vergangenheit zurueckgehen und wie weit die Teile auseinanderliegen
  - fuer jedes Teil berechnen wir den zugehoerigen `index` um eine Position aus der Liste von 1. auszulesen
  - wir setzen die Position des Teils auf den Wert aus der Liste aus 1. an diesem Index

Na dann: Jetzt wo der Plan feststeht kann es ja losgehen. Zunaechst definieren wir die Liste der vergangenen Positionen im `GameState`:

```rust 
pub struct GameState {
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    past_positions: Vec<Vec2>, // neu!
}

pub fn setup(c: &mut GameContext) {
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    c.state.past_positions = vec![]; // neu!
}

pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions } = &mut c.state;
    //                      ^^^^^^^^^^^^^^ neu
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...
}
```

*schaut auf Zettel* 

> dazu legen wir eine Liste fuer die Positionen an 

✅

Ok, naechster Schritt: jedes Frame fuegen wir die aktuelle Position in die Liste ein.

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions } = &mut c.state;
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    past_positions.push(*center); // neu
}
```

Ok, krass. Das ist ja voll easy, wenn man einen Plan hat. Check ✅

Zum Schluss wollen wir noch die Liste auf (erstmal) 100 Elemente beschraenken. Wenn wir das nicht tun, wird unsere Liste unendlich weit wachsen bis der komplette Speicher des Computers voll ist und das Programm oder der Rechner abstuerzt.

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions } = &mut c.state;
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    past_positions.push(*center);

    if past_positions.len() > 100 { //
        past_positions.remove(0);   // neu
    }                               //
}
```

Und damit haetten wir Teil 1 unseres Plans schon mal abgehakt ✅

Kommen wir nun zu Teil 2, der etwas trickier wird. Erstmal definieren wir uns ein paar Variablen, die folgende Dinge tun 

>
> - wir legen eine Anzahl an Teilen der Schlange fest 
> - wir legen eine Schrittgroesse fest, die sagt wie weit wir in die Vergangenheit zurueckgehen und wie weit die Teile auseinanderliegen
>

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions } = &mut c.state;
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    let num_parts = 10; // neu
    let step_size = 20; // neu

    past_positions.push(*center);

    if past_positions.len() > 100 {
        past_positions.remove(0);
    }                            
}
```

Anhand dieser Variablen koennen wir nun auch nochmal die random gewaehlte `100` aus Teil 1 anpassen, da wir berechnen koennen wie viele Elemente wir maximal brauchen. Das ist ganz einfach beschraenkt durch `num_parts * step_size`.

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions } = &mut c.state;
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    let num_parts = 10;
    let step_size = 20;

    past_positions.push(*center);

    //                        vvvvvvvvvvvvvvvvvvvvvvv - angepasst
    if past_positions.len() > (num_parts * step_size) {
        past_positions.remove(0);
    }                            
}
```

Nun brauchen wir noch eine Liste um die Positionen des Rests der Schlange zu speichern. Dieser kann genauso zum Programm hinzugefuegt werden wie `past_positions` auch schon. Traust du dir schon zu das selbst zu probieren? Versuch es doch mal bevor du dir die Loesung anschaust!

<details>
<summary> Loesung </summary>

```rust 
pub struct GameState {
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    past_positions: Vec<Vec2>,
    tail_parts: Vec<Vec2>, // neu!
}

pub fn setup(c: &mut GameContext) {
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    c.state.past_positions = vec![];
    c.state.tail_parts = vec![]; // neu!
}

pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions, tail_parts } = &mut c.state;
    //                                      ^^^^^^^^^^ neu
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...
}
```

</details>

Der naechste Schritt ist mithilfe der `step_size` die richtigen Stellen in `past_positions` Liste zu berechnen, von denen wir die Daten bekommen wollen.

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions, tail_parts } = &mut c.state;
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    let num_parts = 10;
    let step_size = 20;

    past_positions.push(*center);

    if past_positions.len() > (num_parts * step_size) {
        past_positions.remove(0);
    }                            

    for i in 0..num_parts {        //
        let index = i * step_size; // neu!
    }                              //
}
```

und im Anschluss sollten wir diesen `index` auch nutzen, um den entsprechenden Eintrag in `tail_parts` zu updaten oder einzufuegen.

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions, tail_parts } = &mut c.state;
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    let num_parts = 10;
    let step_size = 20;

    past_positions.push(*center);

    if past_positions.len() > (num_parts * step_size) {
        past_positions.remove(0);
    }                            

    for i in 0..num_parts {       
        let index = i * step_size;
        let new_tail_position = past_positions.get(index).copied().unwrap_or_default();
        let old_tail = tail_parts.get_mut(index);

        if old_tail.is_none() {
            tail_parts.push(new_tail_position);
        } else {
            let mut old_tail_unwrapped = old_tail.unwrap();
            *old_tail_unwrapped = new_tail_position;
        }
    }                             
}
```

Damit haben wir auch schon komplett Teil 2 abgehakt ✅ Als letzten Schritt muessen wir nun nur noch diese Daten verwenden, um wirklich den Rest der Schlange zu zeichnen.

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions, tail_parts } = &mut c.state;
    
    // ...
    // ... hier steht der Code von letztem Mal
    // ...

    let num_parts = 10;
    let step_size = 20;

    past_positions.push(*center);

    if past_positions.len() > (num_parts * step_size) {
        past_positions.remove(0);
    }                            

    for i in 0..num_parts {       
        let index = i * step_size;
        let new_tail_position = past_positions.get(index).copied().unwrap_or_default();
        let old_tail = tail_parts.get_mut(index);

        if old_tail.is_none() {
            tail_parts.push(new_tail_position);
        } else {
            let mut old_tail_unwrapped = old_tail.unwrap();
            *old_tail_unwrapped = new_tail_position;
        }
    }                             

    for tail in tail_parts {
        draw_rect(*tail, Vec2::ONE, Color::rgb(0.0, 0.1, 0.2), 0);
    }
}
```

![Snake mit mehr als einem Teil](./imgs/011-snake.png)

# 6. Kuchen und Kollisionserkennung

## Zufaellige Kuchen

Als naechstes brauchen wir etwas zu Essen fuer unsere Snake. Unser spontaner Einfall war es ihr einen Kuchen zu geben. Der Kuchen soll immer an einer zufaelligen Position erscheinen. Damit wir die Position wieder ueber mehrere frames speichern koennen, brauchen wir erstmal wieder ein neues Feld in unserem `GameState`. Ich denke, dass es inzwischen schon einfacher faellt das selbst zu machen. Deshalb lassen wir hier jetzt mal diesen Teil aus. Kleine Hinweise:

- wir fuegen folgendes im `GameState` hinzu : `cake_center: Vec2`
- wenn du nicht mehr weiter weisst, orientiere dich an einem der anderen Male von weiter oben

Nun koennen wir diese Position nutzen, um einen Kreis zu zeichnen:

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions, tail_parts, cake_center } = &mut c.state;
    
    // ...
    // ... anderer Code
    // ...

    draw_circle(*cake_center, 0.5, Color::rgb(1.0, 1.0, 1.0), 1);
}
```

Damit der Kreis nun wirklich an einer zufaelligen Position auftaucht, muessen wir in `setup` auch wirklich die Variable auf eine zufaellige Position setzen. Dazu gibt es in `comfy` die `random_range` Funktion. Sie nimmt eine untere und eine obere Grenze und gibt einen zufaelligen Wert zwischen diesen beiden Werten zurueck. Sie wird zum Beispiel so hier verwendet:

```rust
let zahl = random_range(0.0, 10.0);
```

Hierbei wird Zahl eine Kommazahl zwischen `0.0` und `10.0` sein. Nun nutzen wir das einfach, um die `x` und `y` Koordinaten von `cake_center` zu setzen:

```rust 
pub fn setup(c: &mut GameContext) {

    // ...
    // ... anderer Code
    // ...

    c.state.cake_center.x = random_range(-5.0, 5.0);
    c.state.cake_center.y = random_range(-5.0, 5.0);
}
```

![Ein weisser Kreis mit zufaelliger Position ist neben der Snake zu sehen](./imgs/012-randomcake.png)

## Kollision - Ein kleiner Exkurs

### Das Problem

Der Einfachheit halber haben wir den Kopf der Snake in einen Kreis geaendert. Das ist bereits auf dem letzten Bild zu sehen. Dies wird uns jetzt helfen die Kollision zwischen dem Kopf und dem Kuchen ordentlich zu entdecken. Die Kollision zwischen zwei Kreisen kann naemlich ziemlich einfach berechnet werden. Und `comfy` bietet uns wie immer auch noch Funktionalitaeten um das sogar noch mehr zu vereinfachen.

Zunaechst schauen wir uns erstmal die beiden moeglichen Faelle an:

1. Die zwei Kreise (Kopf der Snake und Kuchen) kollidieren

![Zwei Kreise die ueberlappen](./imgs/013-collidingcircles.png)

2. Die zwei Kreise kollidieren nicht

![Zwei Kreise die nicht ueberlappen](./imgs/014-noncollidingcircles.png)

### Die Loesung

Nun haben wir uns folgende Strategie fuer den Kollisions-Check im GTA erarbeitet: 

1. Ueber den Satz des Pythagoras kann man sich die Laenge der Strecke zwischen den zwei Kreismittelpunkten errechnen. Diese Laenge `L` ist die Distanz zwischen den zwei Kreisen. 

![Satz des Pythagoras fuer Kreisabstand](./imgs/015-pythagoras.png)

2. Nun sagen wir das `S` die Summe der Radien der beiden Kreise ist. `S = r1 + r2`

![Summe der Radien](./imgs/016-sumradius.png)

3. Nun machen wir eine Fallunterscheidung: 

  - Ist die Distanz `L` groesser als die kombinierten Radien `S`, dann kollidieren die Kreise nicht

  ![Kreise kollidieren](./imgs/017-nocollisionsolution.png)

  - Ist die Distanz `L` kleiner als die kombinierten Radien `S`, dann kollidieren die Kreise

  ![Kreise kollidieren](./imgs/018-collisionsolution.png)

4. Das war's auch schon!

## Kollision im Code

Wie gesagt hilft uns `comfy` etwas bei der Implementierung unserer Theorie von oben aus. Wir muessen nicht den Satz des Pythagoras in Code schreiben. Der `Vec2` Typ in `comfy` kommt mit einer praktischen Funktion names `distance`, die einen anderen Punkt annimmt und uns die Distanz zu diesem Punkt ausgibt. Sie wird wiefolgt genutzt:

```rust
let a = Vec2::new(1.0, 0.0);
let b = Vec2::new(3.0, 0.0);

let dist = a.distance(b);

// dist == 2.0
```

Damit koennen wir also schnell die Distanz zwischen Kopf der Snake und Kuchen berechnen:

```rust 
// ...

let dist = head.distance(cake_center);

// ...
```

Nun brauchen wir noch die Summe der Radien von Kopf- und Kuchenkreis. Da wir fuer beide fest den Radius `0.5` gewaehlt haben, ist die Summe einfach `1.0`.

```rust 
// ...

let sum_radii = 0.5 + 0.5;

// ...
```

Als letztes koennen wir die Fallunterscheidung von oben mit einem einfachen Vergleichsoperator implementieren und bekommen daraus einen `bool` Wert zurueck. `bool` Werte koennen nur entweder `true` (wahr) oder `false` (falsch) sein. Das heisst im Code

```rust 
// ...

let is_colliding = dist < sum_radii;

// ...
```

kann es sein, dass

- `is_colliding` den Wert `true` annimmt, wenn die Distanz der Kreise kleiner der Summe der Radien ist
- `is_colliding` den Wert `false` annimmt, wenn die Distanz der Kreise groesser der Summe der Radien ist

Basiered auf dem `is_colliding` Wert, koennen wir nun zum Beispiel einfach mal eine andere Farbe fuer den Kuchen waehlen:

```rust 
// ...

let cake_color = if is_colliding { Color::rgb(0.0, 0.0, 1.0) } else { Color::rbg(1.0, 1.0, 1.0) };

draw_circle(*cake_center, 0.5, cake_color, 1);

// ...
```

![Der Kuchen wird blau wenn die Snake mit ihm kollidiert](./imgs/019-collisionblue.png)

Der gesamte Code ist nun 

```rust 
pub fn update(c: &mut GameContext) {
    let GameState { center, past_positions, tail_parts, cake_center } = &mut c.state;
    
    // ...
    // ... anderer Code
    // ...

    let dist = head.distance(cake_center);
    let sum_radii = 0.5 + 0.5;

    let is_colliding = dist < sum_radii;

    let cake_color = if is_colliding {
        Color::rgb(0.0, 0.0, 1.0)
    } else {
        Color::rbg(1.0, 1.0, 1.0)
    };

    draw_circle(*cake_center, 0.5, cake_color, 1);
}
```

## Springende Kuchen

Damit der Kuchen an eine neue Position springt, wenn wir mit ihm kollidieren, braucht es nun nicht mehr viel Code. Wir muessen einfach nur die Position wie in `setup` auf eine zufaellige Position setzen, wenn `is_colliding` wahr ist.

```rust 
    if is_colliding {
        *cake_center.x = random_range(-5.0, 5.0);
        *cake_center.y = random_range(-5.0, 5.0);
    }
```

## Wachsende Schlangen

Um die Schlange nun wachsen zu lassen, muessen wir auch nicht mehr viel machen. Es reicht folgendes zu tun: 

- `num_parts` muss in den `GameState` ausgelagert werden (wir wollen es ja aendern)
- wir setzen `num_parts` am Anfang auf `1`
- immer, wenn `is_colliding` wahr ist, dann fuegen wir ein part hinzu (also wir addieren `1` auf `num_parts`)

Im Code oben ergaenzen wir

```rust 
    if is_colliding {
        *cake_center.x = random_range(-5.0, 5.0);
        *cake_center.y = random_range(-5.0, 5.0);
        *num_parts += 1;
    }
```
