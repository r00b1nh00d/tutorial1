# KISS_MINT Calliope Adventskalender
## ~avatar avatar @unplugged
**Herzlich Willkommen zum KISS_MINT Calliope Adventskalender** <br>
![Titelbild](https://github.com/r00b1nh00d/tutorial1/blob/master/73_cut_long.JPG?raw=true) <br>
Bis Weihnachten erwarten dich hier 24 kleine Projekte zum selber programmieren. <br>
Die meisten Projekte kannst du auch ohne einen eigenen Calliope ausprobieren. Nur wenn mal etwas an den Calliope angeschlossen werden soll brauchst du selbst einen Calliope. <br>
Falls du schon einen besitzt aber noch nicht viel damit gemacht hast schau dich gerne auch mal auf [calliope.cc](calliope.cc) um. <br>
In der [Übersicht](https://calliope.cc/calliope-mini/uebersicht) findest du beispielsweise, was der Calliope alles kann. <br>
Unter [Programmieren](https://calliope.cc/programmieren/mobil) wird dir z.B. auch gezeigt wie du den Calliope über das Smartphone oder Tablet programmierst.<br>

## ~@unplugged
Bei einigen Projekten wird auch mal etwas gebastelt dazu könntest du folgende Dinge benötigen: 
 **Elektronik:** <br>        
 Calliope mini <br>       
 Jumperkabel   <br>      
 Dünne Kabel   <br>       
 WS2812b RGB LED Band<br> 
 Servo Motor     <br> 

**Werkzeug** <br>
Bastelmaterial (Schere, Stift..)<br>
Alleskleber/ Heißkleber<br>
Lötkolben+Lötzinn<br>
ggf. Holzsäge<br>

**Sonstiges:**
Buntes Tonpapier <br>
Bindfaden<br>
Sperrholz(Pappel)<br>
Batterie+Halter <br>
Weihnachtsplätzchen<br>
Karton <br>


## ~ @unplugged 
In diesem Tutorial fangen wir ganz einfach mit unserem ersten Programm an. Bis Weihnachten haben wir ja noch etwas Zeit komplexere Programme zu schreiben. <br> 
Bis dahin wirst du auch lernen wie du Variablen, wenn-dann-Bedingungen, Schleifen und Listen nutzt oder Spiele programmierst. <br>



## ~ @unplugged 
Dein Calliope hat einen kleinen Bildschirm mit 5x5 (also zusammen 25) LED's. Mit diesem Bildschirm kannst du auch wie auf deinem Smartphone Bilder anzeigen. <br>
Allerdings wären dies nur 5 mal 5 Pixel, dennoch kannst du damit so einige Bilder oder Symbole anzeigen. <br>
![erstes Programm](https://github.com/r00b1nh00d/tutorial1/blob/master/erstesProgramm.gif?raw=true)

## Schritt 1
In deinem Arbeitsbereich sollten bereits die Blöcke ``||basic:beim Start||`` und ``||basic:dauerhaft||`` liegen. <br>
Um ein Bild anzeigen zu lassen, kannst du aus der Gruppe ``||basic:Grundlagen||`` den Block ``||basic:zeige Leds||`` in deinen ``||basic:dauerhaft||`` Block per Drag and Drop schieben. <br>
Um einen Block, wie beispielsweise den ``||basic:beim Start||`` zu löschen kannst du ihn auch einfach wieder anklicken und angeklickt zurück in die Blockansicht schieben. Währenddessen wird dieser Bereich rot uns zeigt ein Mülleimersymbol. <br>

```blocks
basic.forever(function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        `)
})
```

## Schritt 2
In dem Block ``||basic:zeige Leds||`` kannst du die einzelnen Felder anklicken, diese werden dann ausgefüllt und ist somit "aktiv", der Calliope zeigt dir dies auch im Simulator an. Klickst du ein ausgeülltes Feld neu an wird es wieder deaktiviert. <br>
Versuche nun die Felder so anzuklicken, dass ein Herz angezeigt wird. 
```blocks
basic.forever(function () {
  basic.showLeds(`
        . # . # .
        # # # # #
        # # # # #
        . # # # .
        . . # . .
        `)
})
```

## Schtitt 3
Lass nun das Herz blinken indem du abwechselnd das Herz und nichts anzeigen lässt. Damit dein Auge 

```blocks
basic.forever(function () {
  basic.showLeds(`
        . # . # .
        # # # # #
        # # # # #
        . # # # .
        . . # . .
        `)

  basic.showLeds(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        `)
})
```
## Schritt 4 
Jetzt kannst du selbst Weihnachtliche Bilder erstellen. <br>
Ideen dazu wären z.B. ein Geschenk, ein Weihnachtsbaum, ein Rentier oder ein Glöckchen.

## Schritt 5
Hier siehst du jetzt in der Hinweis-box ein paar Möglichkeiten 
```blocks
basic.forever(function () {
    basic.showLeds(`
        # . # . .
        . # . . .
        # # . . #
        . # # # .
        . # . # .
        `)
    basic.pause(100)
    basic.showLeds(`
        . . . . .
        . . . . .
        # . # # #
        # . # . #
        . # # # #
        `)
    basic.pause(100)
    basic.showLeds(`
        . . # . .
        . # # # .
        . # # # .
        . # # # .
        # # # # #
        `)
    basic.pause(100)
    basic.showLeds(`
        . # . # .
        # # # # #
        # # # # #
        . # # # .
        . . # . .
        `)
    basic.pause(100)
    basic.showLeds(`
        . . # . .
        # . # . #
        . # # # .
        # . # . #
        . . # . .
        `)
    basic.pause(100)
})

```
## Schritt 6
Einen Text anzeigen ist genau so einfach wie ein Symbol anzuzeigen. <br>
Um diesen in dein Bisherigen Programmcode einzubinden bietet es sich an, aus dem Bereich ``||input:Eingaben||`` den Block ``|input: wenn Knopf A gefrückt||`` zu verwenden.
In diesen Block kannst du den Block ``||basic: zeige Text||`` hineinschieben und in das Feld deinen Text schreiben. Jetzt beginnt der Calliope den Text anzuzeigen sobald du dein Knopf A drückst
```blocks

input.onButtonPressed(Button.A, function () {
    basic.showString("MERRY CHRISTMAS")
})
```
## Schritt 7
Wenn du dir im Dauerhaft-Block noch die Bildchen anzeigen lässt kann es sein, dass es etwas komisch aussieht wenn der Calliope nun anfängt den Text anzuzeigen. Um dies etwas schöner aussehen zu lassen kannst du vor dem Text anzeigen noch den ``||basic:Bildschirminhalt löschen||``. <br>
Diesen Block findest du, wenn du bei ``||basic:Grundlagen||`` auf ``||basic:°°° mehr||`` klickst.
```blocks
input.onButtonPressed(Button.A, function () {
    basic.clearScreen()
    basic.showString("MERRY CHRISTMAS")
})

```

## ~ @unplugged 
Um dein Programm aud den Calliope zu bekommen musst du im unteren Bildschirmbereich des MakeCode Editors auf ``||basic: Herunterladen||``klicken. <br>
Jetzt wird dein Programm als mini- .... .hex Datei gespeichert. Diese wird in deinem Downloadsordner gespeichet. <br>
Von diesem Ordner kannst du die Datei aud deinen, über USB angeschlossenen Calliope schieben qiw beim kopieren bzw. Verschieben von Dateien auf einen USB-Stick.
![BildSpeichern](https://github.com/r00b1nh00d/tutorial1/blob/master/Speichern.PNG?raw=true)


## ~ @unplugged 
Um nochmal zu sehen wie du ein Programm erstellst und speicherst schau dir auch gerne dieses Video an: <br>
[Video](https://www.youtube.com/watch?v=X8NxRAL4snk)

Viel Spaß noch beim weiteren Programmieren :-)
