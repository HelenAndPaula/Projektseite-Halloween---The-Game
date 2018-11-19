# Projektseite Halloween - The Game

<img width="955" alt="bildschirmfoto 2018-11-18 um 16 42 30" src="https://user-images.githubusercontent.com/42578525/48674838-fc716100-eb50-11e8-8abe-c364ddc953ff.png">

## Idee

Unsere Aufgabe für die erste Abgabe war es, uns mit der Technik des Programmierens auseinanderzusetzen und mit Hilfe der erlernten 
Erkenntnisse, ein Spiel oder Ähnliches zu programmieren. 

Da wir beide uns zum ersten Mal mit dem Programmieren an sich beschäftigt haben, haben wir zunächst mehrere Stunden mit der Wahl eines Programms (The Beauty and Joy of Computing, https://snap.berkeley.edu/snapsource/snap.html# ) verbracht und versucht dieses zu verstehen, indem wir den dazugehörigen Onlinekurs bearbeitet haben. 

Nach der Methode des "learning by doing" habe wir zunächst meherere verschiedene kleine Projekte ausprobiert, sodass wir erst 
Anfang Oktober mit unserem richitgen Spiel begannen, wobei wir die aus den verherigen Projekten gewonnenen Strategien nutzten. 

Da nun Halloween immer näher rückte, entschieden wir uns, ein "gruseliges" Spiel zu programmieren, welches vor allem für Kinder 
geeignet ist. 

## Programm

Nach einiger Recherche haben wir uns für das Programm Snap! und den dazugehörigen Onlinekurs "The Beauty and Joy of Computing" entschieden. Während der Onlinekurs ausschließlich auf Englisch verfasst ist, lässt sich das Programm auch auf Deutsch umstellen.

<img width="1278" alt="bildschirmfoto 2018-11-18 um 12 09 25" src="https://user-images.githubusercontent.com/42578525/48671585-e0f35f80-eb2a-11e8-9746-e4ef1091e5f8.png">

Snap! ist eine visuelle Blockprogrammiersprache, die sich besonders für Einsteiger eignet, da die einzelnen Befehle aus bereits vorhandenen Blöcken zusammengesetzt werden, die sich in acht Kategorien gliedern: Bewegung, Steuerung, Aussehen, Fühlen, Klang, Stift, Operatoren und Variablen. 

<img width="189" alt="bildschirmfoto 2018-11-18 um 12 03 21" src="https://user-images.githubusercontent.com/42578525/48671534-016eea00-eb2a-11e8-9b85-b7a02714d0e4.png">

Aus jeder der Kategorien, denen der Übersicht halber auch je eine Farbe zugeteilt ist, lassen sich eine Vielzahl an Befehlen wählen und per Drag and Drop zusammensetzten. Die Befehle gelten dabei zum beispiel für eine bestimmt Figur oder den Hintergrund, die sich individuell oder aus vorhandnenen Vorlagen wählen lassen.

## Umsetzung der Idee - Konzept

Nachdem wir uns für ein Programm und eine Spielidee entschieden hatten, planten wir die Umsetzung und den Ausbau der Idee. 

### Gegner: Fledermäuse 
In den Vorlagen der Kostüme von Snap! fanden wir vier verschiedene Fledermauskostüme, aus denen sich eine fleigende, mit den Flügeln schlagende Fledermaus annimieren ließ. 

<img width="110" alt="bildschirmfoto 2018-11-18 um 12 43 46" src="https://user-images.githubusercontent.com/42578525/48671949-b48e1200-eb2f-11e8-8ae5-1c54f543aa93.png"> <img width="356" alt="bildschirmfoto 2018-11-18 um 12 41 04" src="https://user-images.githubusercontent.com/42578525/48671908-42b5c880-eb2f-11e8-90f1-36633de2298c.png"> 
<img width="430" alt="bildschirmfoto 2018-11-18 um 12 44 00" src="https://user-images.githubusercontent.com/42578525/48671946-afc95e00-eb2f-11e8-9236-504e06f8ee98.png">

Diese waren der Grundbaustein unseres Spieles. Erst danach wählten wir ein Gespenst als Spielfigur und einen Kürbis als Ziel, welches der Geist erreichen muss. Somit ergaben sich folgende Figuren:

<img width="375" alt="bildschirmfoto 2018-11-18 um 12 59 51" src="https://user-images.githubusercontent.com/42578525/48672099-edc78180-eb31-11e8-94e0-ca799e994fe0.png">

Nachdem wir nun sowohl die Figuren sowie den Inhalt des Spiels festgelegt hatten, versuchten wir zunächst, die Fledermäuse als Gegner zu progrmmieren. Dazu nutzten wir die verschiednen Kostüme (s. oben) und gaben den Befehl, dass die Fledermäuse sich jeweils um zwei Schritte bewgen sollten, an den Rändern des Spielfeldes abprallen sollen und sich dabei die verschiedenen Fledermäuse auf verschienden Höhen bewegen.

<img width="228" alt="bildschirmfoto 2018-11-18 um 14 57 45" src="https://user-images.githubusercontent.com/42578525/48673504-6afaf280-eb42-11e8-9ce8-1d4d9e5eb35c.png">

Somit hatten wird die Grundlage eines sich bewgenden Gegners geschaffen.

### Hauptfigur: Geist

ALs nächstes programmierten wir den Geist als Hauptfigur. Unser Ziel war es dabei, dass der Spieler den Geist mit den Pfeiltasten steuern kann, um den Kürbis zu erreichen und den FLedermäusen auszuweichen. Dabei entspricht die Richtung der Pfeiltaste der Bewegungsrichtung. 

Dazu nutzten wir den Control-Block "Wenn Pfeiltaste nach (Richtung) gedrückt" und gaben an dass sich das Gespenst in diesem Falle zwei Schritte in die jeweilige Richtung bewegen sollte. 

<img width="575" alt="bildschirmfoto 2018-11-18 um 15 15 02" src="https://user-images.githubusercontent.com/42578525/48673758-07be8f80-eb45-11e8-866a-d7870e44af99.png">

Zudem sollte das Gespenst auf Berührungen mit den Fledermäuses reagieren. Dazu wählten wir ein zweites Gespenst aus den verfügbarene Kostümen. Sobald dich Fledermaus und Geist berühren, verschwindet das Gespenst kurz und wechselt dann für 0,3 Sekunden zu einem anderen Kostüm, das den Geist wütend zeigt. Danach wechselt es zurück zu seinem vorherigren Kostüm. Um dies darzustellen nutzen wir den Control-Befehl "Wenn berühre "bat"" und gaben danach die auszuführenden Befehle an. Diesen Befehl programmierten wir für alle Fledermäuse. 

<img width="575" alt="bildschirmfoto 2018-11-18 um 15 15 02" src="https://user-images.githubusercontent.com/42578525/48674001-16f30c80-eb48-11e8-9ec3-c09ac58221eb.png">

### Ziel: Kürbis

Die Aufgabe des Spieler sollte es sein, als Gepenst möglichst oft den Kürbis als Ziel zu berühren. Den Kürbis suchten wir uns aus dem Internet und setzten ihn als Kostüm ein. Anschließend entschieden wir uns, statt mehrerer Kürbisse nur einen zu wählen, der nach jeder Berührung durch den Geit an eine neue zufällige Position wechselt, zu Beginn jeder Runde jedoch an der selben Koordinate (-50⎢100) starten. Da wir als Start des Spiels das Drücken der Leertaste festgelegt hatte, nutzten wir den Control-Block "Wenn Taste Leertaste gedrückt" und den Motion-Block "Gehe zu x: -50, y: 100), wobei der Kürbis auf 30% seiner Größe reduziert werden sollte: Look-Block "setzt Grüße auf 30%".

<img width="221" alt="bildschirmfoto 2018-11-18 um 16 15 21" src="https://user-images.githubusercontent.com/42578525/48674484-2d4f9700-eb4d-11e8-8791-936b1a8b5194.png">
Um den Kürbis an eine zufällige Stelle springen zu lassen, wählten wir den Sensing-Block "Wenn berühre Sprite(2)" und den Look-Block "verstecken", damit der Kürbis zunäxhst kurz verschwindet. Darauf folgt der Motion-Block "gehe zu zufällige Position" und die Auflösung des Versteckens durch den Befehl "anzeigen". Um den Kürbis dabei innerhalb des Spielfelds zu halten, nutzten wir zudem den Befehl "Pralle von Rand ab". 

<img width="218" alt="bildschirmfoto 2018-11-18 um 16 20 20" src="https://user-images.githubusercontent.com/42578525/48674558-e01ff500-eb4d-11e8-9e52-6dc26096f04d.png">

### Hintergrund (Bühne)

Da es sich bei unserem Spiel um ein Halloween-Spiel handelt, wählen wir einen Nachthimmel als Hintergrund, den wir aus dem Internet heraussuchten. Mithilfe des in Snap! intergrierten Editors bearbeiteten wir den Hintergrund und passten ihn größentechnisch an. Der Hintergrund ist dabei absichtlich etwas verschwommen, damit die Figuren besser erkennbar in den Vordergrund treten.

![himmel 2](https://user-images.githubusercontent.com/42578525/48674797-7b19ce80-eb50-11e8-9056-cd3fc11a5f9c.png)

### Punktesystem und Zeit

Um dem Spiel ein Ziel zu geben, welches der Spieler erreichen muss, haben wir uns zudem ein Punktesystem überlegt. Der Spieler startet mit 0 Punkten und gewinnt immer zwei Punkte, wenn er den Kürbis berührt, verliert jedoch einen wenn er mit den Fledermäusen in Kontakt kommt. Da wir es bisher nicht geschafft haben, dem Geist Leben abzuziehen, begrenzt sich die Spielzeit auf 60 Sekunden, nach denen das Spiel stoppt. 

Um das Punktesystem zu erstellen, errichteten wir zunächst die neue Variable "Punkte" und gaben an wie sich diese ändern sollte. Das selbe taten wir mit der Variable "Zeit". 

