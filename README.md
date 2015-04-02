# Alumni-Portal Universität Würzburg
Die Universität Würzburg stellt ihren Studenten, ehemaligen Studenten,
Professoren, Bekannten und Freunden ein eigenes Portal zur Verfügung.
Dieses bietet die Gelegenheit, mit Kommilitonen und Professoren in Kontakt zu bleiben.

Bei dieser Umsetzung handelt es sich nicht um ein offizielles Projekt der Universität Würzburg. Die Idee das Alumni Portal zu überarbeiten entstand im Rahmen einer *Mensch-Computer-Interaktion* Veranstaltung im Wintersemester 14/15.

## Build-Environment
Eine lokale Installation von Node.js (beinhaltet zusätzlich den Package-Manager *npm*) wird zwingend vorausgesetzt. Die Befehle ```node``` und ```npm``` müssen in  ```PATH```hinterlegt und über die Konsole aufrufbar sein.

### Installation von [Yo](http://www.yeoman.io), [Grunt](http://gruntjs.com/) und [Bower](http://bower.io/) via Kommandozeile:

```npm install -g yo bower grunt-cli```

###Installation von MongoDB

Das Portal nutzt als Datenbank MongoDB. Diese muss zuvor auf dem Entwickler-PC installiert werden.

Download: [MongoDB](https://www.mongodb.org/downloads)

Da die Webseite in JavaScript umgesetzt wird und Node.js zum Einsatz kommt, wird für die Programmierung der Datenbank auf *mongoose* zurückgegriffen. Während der Programmierung muss der Prozess *mongod* lokal laufen, um Zugriff auf die Datenbank zu gewährleisten.

### Befehle auf der Kommandozeile:

** Allgemein **

* ```grunt``` führt den Build-Prozess aus
* ```grunt serve``` startet einen lokalen Server und zeigt Vorschau der Seite
* ```grunt serve:dist``` erzeugt eine Vorschau der fertig gebauten Applikation

** Tests **

* ```grunt test``` führt Unit-Tests für Client und Server aus
* ```grunt test:client``` führt nur Unit-Tests des Client aus
* ```grunt test:server``` führt nur Unit-Tests des Server aus

** Ende-zu-Ende Tests **

führe zuerst einmalig ```npm run update-webdriver``` aus
* ```grunt test:e2e``` führt protractor Test aus, die im Ordner *e2e* enthalten sind
