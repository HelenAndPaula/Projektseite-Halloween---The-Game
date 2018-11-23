# Projektseite Halloween - The Game

<img width="955" alt="bildschirmfoto 2018-11-18 um 16 42 30" src="https://user-images.githubusercontent.com/42578525/48674838-fc716100-eb50-11e8-8abe-c364ddc953ff.png">

# *Inhaltsverzeichnis* 

[1.   Idee](#1)  

[2.   Programm](#2)  

[3.   Umsetzung der Idee - Konzept](#3)

[4.   Gegner: Fledermäuse](#4)
 
[5.   Hauptfigur: Geist](#5)

[6.   Ziel: Kürbis](#6)

[7.   Hintergrund (Bühne)](#7)

[8.   Anleitung](#8)
 
[9.   Punktesystem und Zeit](#9)

[10.   Spielende und Endbildschirm](#10)

[11.   Startbildschirm](#11)

[12.   Musik](#12)

[13.   Stundenblog](#13)



## <a name="1"></a> Idee

Unsere Aufgabe für die erste Abgabe war es, uns mit der Technik des Programmierens auseinanderzusetzen und mit Hilfe der erlernten 
Erkenntnisse, ein Spiel oder Ähnliches zu programmieren. 

Da wir beide uns zum ersten Mal mit dem Programmieren an sich beschäftigt haben, haben wir zunächst mehrere Stunden mit der Wahl eines Programms (The Beauty and Joy of Computing, https://snap.berkeley.edu/snapsource/snap.html# ) verbracht und versucht dieses zu verstehen, indem wir den dazugehörigen Onlinekurs bearbeitet haben. 

Nach der Methode des "learning by doing" habe wir zunächst meherere verschiedene kleine Projekte ausprobiert, sodass wir erst 
Anfang Oktober mit unserem richitgen Spiel begannen, wobei wir die aus den verherigen Projekten gewonnenen Strategien nutzten. 

Da nun Halloween immer näher rückte, entschieden wir uns, ein "gruseliges" Spiel zu programmieren, welches vor allem für Kinder 
geeignet ist. 

## <a name="2"></a> Programm

Nach einiger Recherche haben wir uns für das Programm Snap! und den dazugehörigen Onlinekurs "The Beauty and Joy of Computing" entschieden. Während der Onlinekurs ausschließlich auf Englisch verfasst ist, lässt sich das Programm auch auf Deutsch umstellen.

<img width="1278" alt="bildschirmfoto 2018-11-18 um 12 09 25" src="https://user-images.githubusercontent.com/42578525/48671585-e0f35f80-eb2a-11e8-9746-e4ef1091e5f8.png">

Snap! ist eine visuelle Blockprogrammiersprache, die sich besonders für Einsteiger eignet, da die einzelnen Befehle aus bereits vorhandenen Blöcken zusammengesetzt werden, die sich in acht Kategorien gliedern: Bewegung, Steuerung, Aussehen, Fühlen, Klang, Stift, Operatoren und Variablen. 

<img width="189" alt="bildschirmfoto 2018-11-18 um 12 03 21" src="https://user-images.githubusercontent.com/42578525/48671534-016eea00-eb2a-11e8-9b85-b7a02714d0e4.png">

Aus jeder der Kategorien, denen der Übersicht halber auch je eine Farbe zugeteilt ist, lassen sich eine Vielzahl an Befehlen wählen und per Drag and Drop zusammensetzten. Die Befehle gelten dabei zum Beispiel für eine bestimmt Figur oder den Hintergrund, die sich individuell oder aus vorhandnenen Vorlagen wählen lassen.

## <a name="3"></a> Umsetzung der Idee - Konzept

### <a name="4"></a>Gegner: Fledermäuse 
In den Kostüm-Vorlagen von Snap! finden sich vier verschiedene Fledermauskostüme, aus denen sich eine fliegende, mit den Flügeln schlagende Fledermaus annimieren ließ. 

<img width="110" alt="bildschirmfoto 2018-11-18 um 12 43 46" src="https://user-images.githubusercontent.com/42578525/48671949-b48e1200-eb2f-11e8-8ae5-1c54f543aa93.png"> <img width="356" alt="bildschirmfoto 2018-11-18 um 12 41 04" src="https://user-images.githubusercontent.com/42578525/48671908-42b5c880-eb2f-11e8-90f1-36633de2298c.png"> 
<img width="430" alt="bildschirmfoto 2018-11-18 um 12 44 00" src="https://user-images.githubusercontent.com/42578525/48671946-afc95e00-eb2f-11e8-9236-504e06f8ee98.png">

Diese sind der Grundbaustein des Spieles. Erst danach folgten ein Gespenst als Spielfigur und einen Kürbis als Ziel, welches der Geist erreichen muss. Somit ergaben sich folgende Figuren:

<img width="375" alt="bildschirmfoto 2018-11-18 um 12 59 51" src="https://user-images.githubusercontent.com/42578525/48672099-edc78180-eb31-11e8-94e0-ca799e994fe0.png">

Die Fledermäuse haben als Gegner die Aufgabe, sich frei auf dem Spielfeld zu bewegen, sodass der SPieler ihnen ausweichen muss. Dabei sollen sie möglichst realistisch mit den Flügeln schlagen.  Zunächst wird die Größe der Fledermaus durch den Look-Block "setzte Größe auf" auf 25% reduziert, um die der größe des Spielfeldes anzupassen. Aus verschiednen Kostümen lässt sich eine Flugbewegung animieren. Dazu werden insgesamt vier Kostüme genutzt, die die Fledermausflügel in verschiedenen Postionen zeigt. Die Kostüme sind der Übersicht halber von eins bis vier nummeriert. Um eine Flugbewegung darzustellen, werden die Kostüme durch den Look-Block "ziehe Kostüm x an" nacheinander mit einer Wartezeit von je 0.1 Sekunden (Control-Block "warte x Sek.") gewechselt, sodass dabei eine einheitliche Bewegung durch folgende Reihenfolge entsteht: Kostüm 1 - Kostüm 2 - Kostüm 3 - Kostüm 4 - Kostüm 3 - Kostüm 2- ... Somit schlägt die Federmaus mit den Flügeln, sobald die Leertaste gedrückt wird, da dieser Befehl (Wenn Taste "Leertaste" gedrückt") am Anfang des Blocks steht. 

Um die Fledermäuse über das Spielfeld fliegen zu lassen, werden nun zusätzlich Motion-Blocks in einem neuen Befehl verwendet. Auf den Control-Block "Wenn Taste "Leertaste" gedrückt" folgt der Control-Befehl das fortlaufend zwei Motion-Blöcke ausgeführt werden sollen. Der Block "pralle vom Rand ab" sorgt dafür, dass die Fledermäuse im Spielfeld bleiben, der Befehl "gehe 2 Schritte" sorgt für eine kontinuirliche Bewgung über das Spielfeld. 
<img width="228" alt="bildschirmfoto 2018-11-18 um 14 57 45" src="https://user-images.githubusercontent.com/42578525/48673504-6afaf280-eb42-11e8-9ce8-1d4d9e5eb35c.png">

Anschließend lässt sich die programmierte Fledermaus mit der rechten Maustaste anklicken und auf eine beliebige Anzahl klonen.

Somit  wird die Grundlage eines sich bewgenden Gegners geschaffen.

### <a name="5"></a> Hauptfigur: Geist

Als Hauptfigur des Spiels dient ein Geist.  Ziel ist es dabei, dass der Spieler den Geist mit den Pfeiltasten steuern kann, um den Kürbis zu erreichen und den FLedermäusen auszuweichen. Dabei entspricht die Richtung der Pfeiltaste der Bewegungsrichtung. 

Dazu  wird der Control-Block "Wenn Pfeiltaste nach (Richtung) gedrückt" genutzt und angegeben, dass sich das Gespenst in diesem Falle zwei Schritte in die Richtung der Pfeiltaste bewegen soll. Dazu wird zunächst der Control-Block "Wenn Taste "Pfeil nach x" gedrückt" gesetzt und an diesen der Motion-Block "zeige Richtung x" gesetzt. Die Richtung entspricht dabei der Pfeiltaste und wird durch Gradzahlen dargestellt (links: -90, rechts: 90, oben: 0, unten: 180). AUf diesen Befehl folgt erneut der Motion-Block "gehe 2 SChritte" mit der Ergänzung "pralle vom Rand ab". 

<img width="575" alt="bildschirmfoto 2018-11-18 um 15 15 02" src="https://user-images.githubusercontent.com/42578525/48673758-07be8f80-eb45-11e8-866a-d7870e44af99.png">

Zudem sollte das Gespenst auf Berührungen mit den Fledermäuses reagieren. Zur Visualisierung  dient ein zweites Gespenst aus den verfügbarene Kostümen. Sobald sich Fledermaus und Geist berühren, verschwindet das Gespenst kurz und wechselt dann für 0,3 Sekunden zu einem anderen Kostüm, das den Geist wütend zeigt. Danach wechselt es zurück zu seinem vorherigren Kostüm.

Hierbei wird zunächst der Sensing-Block "Wenn berühre "x"" genutzt, wobei x durch die Namen der verschidenen Fledermäuse ersetzt wird. In diesem Fall tritt der Look-Block "verstecken" in Kraft, sodass die Fledermaus kurzzeitig verschwindet bis der Befehl durch den Look-Block "anzeigen" wieder aufgelöst wird. Darauf folgt der Look-Befehl "ziehe Kostüm x" an, dabei wird der Name des Kostüms für den zweiten Geist eingesetzt. Auch hier wird die Größe durch den Befehl "setze Größe auf 30%" reduziert. Durch den Control-Befehl "warte 0.3 Sek." bleibt der Geist für 0.3 Sekunden in diesem Kostüm, danach wechselt er zu seinem normalen Kostüm durch den Betehl "ziehe Kostüm x" an, wobei der ursprüngliche Kostüm-Name eingesetzt wird. 
iesen Befehl programmierten wir für alle Fledermäuse. 

<img width="575" alt="bildschirmfoto 2018-11-18 um 15 15 02" src="https://user-images.githubusercontent.com/42578525/48674001-16f30c80-eb48-11e8-9ec3-c09ac58221eb.png">

### <a name="6"></a> Ziel: Kürbis

Die Aufgabe des Spieler sollte es sein, als Gepenst möglichst oft den Kürbis als Ziel zu berühren. Die Kürbis-Grafik stammt aus dem Internet. Der Kürbis, von dem es nur einen einzigen gibt, wechselt nach jeder Berührung durch den Geit an eine neue zufällige Position, startet jedoch zu Beginn jeder Runde  an der selben Koordinate (-50⎢100) starten. Da  als Start des Spiels das Drücken der Leertaste festgelegt ist, wird der Control-Block "Wenn Taste Leertaste gedrückt" und den Motion-Block "Gehe zu x: -50, y: 100) verwendet, wobei der Kürbis auf 30% seiner Größe reduziert wird: Look-Block "setzt Grüße auf 30%". SOmit startet der Kürbis immer an der selben Stelle. 

<img width="221" alt="bildschirmfoto 2018-11-18 um 16 15 21" src="https://user-images.githubusercontent.com/42578525/48674484-2d4f9700-eb4d-11e8-8791-936b1a8b5194.png">

Um den Kürbis an eine zufällige Stelle springen zu lassen, wird der Sensing-Block "Wenn berühre Sprite(2)" gewählt (Sprite (") = Geist) und der Look-Block "verstecken", damit der Kürbis zunächst kurz nicht sichtbar ist. Darauf folgt der Motion-Block "gehe zu zufällige Position" und die Auflösung des Versteckens durch den Befehl "anzeigen". Um den Kürbis dabei innerhalb des Spielfelds zu halten,  wird zudem den Befehl "Pralle von Rand ab"genutzt. 

<img width="218" alt="bildschirmfoto 2018-11-18 um 16 20 20" src="https://user-images.githubusercontent.com/42578525/48674558-e01ff500-eb4d-11e8-9e52-6dc26096f04d.png">

### <a name="7"></a> Hintergrund (Bühne)

Da es sich bei dem Spiel um ein Halloween-Spiel handelt, dient als Hintergrund ein Nachthimmel , der aus dem Internet stammt (http://node.kg.qq.com/play?s=Xw91uqXy9otdMX4r&g_f=personal). Das Bild wird zunächst im Bereich "Bühne" hochgeladen. Mithilfe des in Snap! intergrierten Editors  wird den Hintergrund der Hintergrund bearbeitet und   größentechnisch angepasst. Der Hintergrund ist dabei absichtlich etwas verschwommen, damit die Figuren besser erkennbar in den Vordergrund treten. 

![himmel 2](https://user-images.githubusercontent.com/42578525/48674797-7b19ce80-eb50-11e8-9056-cd3fc11a5f9c.png)

### <a name="8"></a> Anleitung 

Um  zu Beginn des Spiels alles zu erklären, spricht der Geist mit einer Sprechblase mit dem Spieler. Dazu wird der Control-Befehl "Wenn Taste Leertaste gedrückt" mit dem Look-Befehl "sage "Text" für 3 Sekunden" kombiniert, sodass für 3 Sekunden eine Kurze erklärung zu lesen ist. 

<img width="529" alt="bildschirmfoto 2018-11-19 um 16 48 10" src="https://user-images.githubusercontent.com/42578525/48718115-0d86a480-ec1b-11e8-9564-1185a81e768b.png">

<img width="373" alt="bildschirmfoto 2018-11-19 um 16 49 03" src="https://user-images.githubusercontent.com/42578525/48718126-12e3ef00-ec1b-11e8-802c-024a38a29959.png">

### <a name="9"></a> Punktesystem und Zeit

Um dem Spiel ein Ziel zu geben, welches der Spieler erreichen muss, gibt es zudem ein Punktesystem. Der Spieler startet mit 0 Punkten und gewinnt  zwei Punkte, wenn er den Kürbis berührt, verliert jedoch einen wenn er mit den Fledermäusen in Kontakt kommt. 

Um das Punktesystem zu erstellen, wird zunächst in der Befehl-Kategorie "Variablen"  die neue Variable "Punkte" erstellt. Danach wird festgelgt wie sich die Variable "Punkte" verändern soll: Dazu wird als Start-Befehl wieder der Control-Block "Wenn TAste Leertaste gedrückt" gesetzt und danach fortlaufend (Control-Befehl "fortlaufend") folgender Befehl ausgeführt: Durch den Control-Block "falls berühre x" (x sdurch die Bezeichnung des Kürbis ersetzten) wird nach einer Wartezeit von 0.1 Sekunden durch den Control-Block "warte 0.1 Sek." der Punktestand durch den Variable-Block "ändere "Punkte" um 2" um zwei Punkt erhöht. FPr die Fledermäuse wird der selbe Befehl genutzt, jedoch der Kürbis durch die Fledermaus-Namen ersetzt und der Befehl "ändere "Punkte" um -1" verwendet, um die Punkte zu reduzieren. Die Wartezeit dient dazu, den Punktestand nicht zu schnell zu erhöhen bzw. zu verringern. 

<img width="258" alt="bildschirmfoto 2018-11-19 um 16 15 11" src="https://user-images.githubusercontent.com/42578525/48715886-58ea8400-ec16-11e8-8822-83973431c6d6.png">

<img width="246" alt="bildschirmfoto 2018-11-19 um 16 14 32" src="https://user-images.githubusercontent.com/42578525/48715895-5d16a180-ec16-11e8-84af-58e0021df15b.png">

Als Begrenzung der Spieldauer dient ein Timer von 60 Sekunden. Um diesen zu erstellen, wird zunächst in der Befehl-Kategorie "Variablen"  die neue Variable "Zeit" erstellt. Danach wird festgelgt wie sich die Variable "Punkte" verändern soll: Dazu wird als Start-Befehl wieder der Control-Block "Wenn Taste Leertaste gedrückt" gesetzt und danach fortlaufend (Control-Befehl "fortlaufend") folgender Befehl ausgeführt: Auf den Variablen-Block "ändere Zeit um -1" (Zeit soll rückwärts laufen), folgt der Befehl "warte 1 Sek.", da sich so die Zeit im Abstand von 1 Sekunde und somit richitg ändert.  

<img width="241" alt="bildschirmfoto 2018-11-23 um 17 26 58" src="https://user-images.githubusercontent.com/42578525/48953104-02968180-ef45-11e8-81d5-d8898d0044f7.png">

Damit die Punkte bei jedem Spielbeginn auf null und der Countdown bei 60 steht, fügten wir zudem folgenden Befehl hinzu: 
Auf den der Control-Block "Wenn Taste Leertaste gedrückt" folgt der Variablen-Befehl "Setzte Punkte = 0" und "setze Zeit = 60).

<img width="241" alt="bildschirmfoto 2018-11-23 um 17 30 58" src="https://user-images.githubusercontent.com/42578525/48953268-8e101280-ef45-11e8-800b-17f9c0067fd0.png">


### <a name="10"></a> Spielende und Endbildschirm

Als Spielbegrenzung dient der Timer, sobald dieser Null zeogt, wird alles gestoppt. Dazu wird der Control-Befehl "Wenn Zeit = 0" gesetzt, auf den der Control-Block "stoppe alles" folgt.

<img width="177" alt="bildschirmfoto 2018-11-23 um 17 49 17" src="https://user-images.githubusercontent.com/42578525/48954025-1e4f5700-ef48-11e8-8e33-a8c1b5556091.png">

Zudem verschwinden alle Figuren durch den Befehl  "Wenn Zeit =0"  auf den der Look-Block "verstecken" folgt, wobei diesem Befehl der Befehl "Wenn Taste Leertaste gedrückt" in Kombination mit dem Befehl "anzeigen" vorausgeht, da die Figuren auch auf dem Startbildschirm nicht sichtbar sein sollen. 

<img width="235" alt="bildschirmfoto 2018-11-19 um 16 28 50" src="https://user-images.githubusercontent.com/42578525/48716743-45d8b380-ec18-11e8-9e3a-2810c192cf2a.png">

Je nachdem wie viele Punkte der Spieler erzielt hat, erscheinen nach Spielende zwei verschiedene Hintergründe: Erreicht der Spieler weniger als 20 Punkte, erscheint ein Hintergrund mit der Aufforderung es noch einmal zu versuchen, hat er über 20 Punkte erreicht, wird ihm dazu gratuliert. Bei beiden Hintergründen gibt es die Möglichkeit durch erneutes Betätigen der Leertaste eine neue Runde zu spielen und wirden auf BAsis des normalen Hintergrundes durch einen Text in einem seperaten Programm ergänzt und als neue Grafiken eingsetzt. 

Dazu wird das Bühnen-Skript durch den Control-Befehl "Wenn Leertaste gedrückt" erweitert, auf den zunächst der Control Block "warte bis Zeit =0" und danach ein Control-Block "falls...sonst" folgt. "Falls Punkte > 0", "ziehe Kostüm "Gut gemacht" an", "sonst" "ziehe Kostüm "Nochmal" an. 

<img width="252" alt="bildschirmfoto 2018-11-19 um 16 33 06" src="https://user-images.githubusercontent.com/42578525/48716995-d7482580-ec18-11e8-89c4-45d6aedb82e0.png">

<img width="253" alt="bildschirmfoto 2018-11-17 um 11 50 03" src="https://user-images.githubusercontent.com/42578525/48717083-fb0b6b80-ec18-11e8-8d94-d1cfaac04806.png">

<img width="256" alt="123" src="https://user-images.githubusercontent.com/42578525/48717227-41f96100-ec19-11e8-851f-a86c0f92cd9d.png">

### <a name="11"></a> Startbildschirm

Neben diesen beiden Endbildschirmen gibt es auch einen Startbildschirm, bevor das Spiel beginnt. Dieser zeigt dem Spieler den Titel des Spieles und fordert ihn auf, die Leertaste zu drücken, um zu beginnen. 

<img width="955" alt="bildschirmfoto 2018-11-18 um 16 42 30" src="https://user-images.githubusercontent.com/42578525/48674838-fc716100-eb50-11e8-8abe-c364ddc953ff.png">

Damit auf dem Startbilschirm nicht alle Figuren zu sehen sind, sondern erst beim Drücken der Leertaste erscheinen benutzten wird zudem diese Befehlfolge genutzt: Auf den Control-Block "Wenn Fahne angeklickt" folgt der Look-Befehl "verstecken". Erst Wenn Leertaste gedrückt" folgt der Befehl "anzeigen" und die Figuren werden sichtbar. Diese Befehle wurden für jede Figur eingestellt.  

<img width="236" alt="bildschirmfoto 2018-11-19 um 16 39 50" src="https://user-images.githubusercontent.com/42578525/48717459-c0560300-ec19-11e8-8008-164aa26f4c79.png">

Dasselbe gilt für den Punktestand und die Zeit. 

Sobald der Spieler die Leertaste betätigt, wechselt der Hintergrund zu dem normalen Spielhintergrund. 

<img width="336" alt="bildschirmfoto 2018-11-19 um 16 41 05" src="https://user-images.githubusercontent.com/42578525/48717542-ed0a1a80-ec19-11e8-9153-5bbdf3d11de4.png">

### <a name="12"></a> Musik 

Um das Spiel für den Spieler auch akustisch ansprechend zu gestalten, wird es durch Halloween-Musik von YouTube (https://www.youtube.com/watch?v=3LpF3lf3cRQ&t=104s) ergänzt, welche die gesamte Zeit im Hintergrund läuft. DAzu wurde im Skript der Bühne der Control-Befehl "fortlaufend" genutzt und der "Sound"-Befehl "spiele Klang x". 

<img width="220" alt="bildschirmfoto 2018-11-19 um 16 46 55" src="https://user-images.githubusercontent.com/42578525/48717976-be407400-ec1a-11e8-859d-d60c1fcc554f.png">

### <a name="13"></a> Stundenblog

Anbei findet sich der Link zu unserem [Stundenblog](https://github.com/HelenAndPaula/Stundenblog/blob/master/README.md), indem wir jede Stunde unsere einzelnen Arbeitsschritte festgehalten haben:

<img width="304" alt="bildschirmfoto 2018-11-19 um 17 01 45" src="https://user-images.githubusercontent.com/42578525/48719047-daddab80-ec1c-11e8-8fd0-6d05e11a8e1a.png">

<img width="936" alt="bildschirmfoto 2018-11-19 um 17 01 57" src="https://user-images.githubusercontent.com/42578525/48719050-ddd89c00-ec1c-11e8-9961-b95bc6e2d711.png">
