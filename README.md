´´e´nformatik-12.1 - Stundenprotokoll


### Dienstag, der 21.08.2018
In der ersten Doppelstunde Informatik gab Herr Buhl uns zunächst eine kleine Einführung und erläuterte und das Vorgehen im nächsten Schuljahr. Daraufhin hatten wir etwas Zeit uns mit seiner eigenen Seite zum Thema "Wege durch den Informatikunterricht mit Herrn Buhl" (https://github.com/jbuhl/InformatikUnterricht) zu beschäftigen. Auf dieser konnten wir uns mit einigen möglichen Programmen auseinandersetzen, was wir auch fleißig taten. Für uns standen zunächst auf Grund unser sehr eingeschränkten Erfahrungen im Programmieren, Greenfoot und Applab im Fokus.

### Monatg, der 27.08.2018
Heute haben wir uns mit den beiden Programmen näher auseinandergesetzt, die wir gestern für uns geeignet erschienen und sind gemeinsam zu dem Schluss gekommen, dass wir lieber mit Applab als mit Greenfoot arbeiten würden. Die nähere Auseinandersetzung mit beiden Programmen bestand überwiegend daraus, dass wir zum  Beispiel auf Applab mit Buttons und Slidern herumprobiert haben und die generelle Funktionsweise des Programms verstehen wollten. 

### Dienstag, der 28.08.2018
Während unserer Arbeit auf Applab, haben wir auf der seite code.org auch Gamelab entdeckt. Gamelab ist im Gegensatz zu Applab, wie der Name schon sagt tendenziell besser für die Programmierung eines Spiels geeignet, durch die mögliche Erstellung von Sprites. Nun standen wir erneut vor einer Entscheidung und sind zu dem Schluss gekommen, dass wir lieber ein Spiel erstellen möchten. 

### Sonntag, der 02.09.2018
Auch außerhalb des Unterrichts haben wir uns mit Informatik beschäftigt. An diesem Sonntag entstand unser erstes richtiges Konzept. Das Spiel sollte ein "Jump 'n Run" werden. Wir begannen auch direkt mit der Umsetzung. Zunächst erstellten wir den Hintergrund, eine Sonne, einen ersten Untergrund und einen Stein. (BILD) Als "Spielfigur" sollte ein Sprite dienen, für den wir eine Animation von Gamelab nutzten, die einen Elch darstellte. Dieser sollte natürlich auch steuerbar sein. Die Steuerung setzten wir mit "if-Klauseln" auf die Pfeiltasten. (BILD) Als erstes Feature programmierten wir, dass der Elch stirbt, sobald er herunterfällt oder die Sonne berührt. Geschieht dies erscheint eine "Todesnachricht" (Wasted) und man hört einen Sound. Außerdem verschwindet der Stein, wenn der Elch diesen berührt und der Elch wird zu einem Foto von Adriana. 

### Montag, der 03.09.2018
Heute haben wir versucht den Sprung dynamischer und natürlicher aussehen zu lassen. Leider sind wir nicht zu dem gewünschten Ergebnis gekommen. (Screenshot/GIF)

### Samstag, der 08.09.2018
Um das Spiel insgesamt flüssiger scheinen zu lassen, haben wir heute die Kamera auf den Sprite "Elch" fixiert. Dies führt dazu, dass nun der "Elch" im ständigen Mittelpunkt des Spiels befindet und sich der Hintergrund und die Böden ihm "hinterherbewegen". Dadurch haben wir das Spiel auf der horizontalen Ebene theoretisch "open end". 
  
### Sonntag, der 09.09.2018
Dadurch, dass wir am letzten Montag am Sprung erneut gescheitert sind, haben wir uns heute noch einmal an diese Thematik herangewagt, sind leider jedoch wieder "gescheitert". Trotzdem haben wir weitere Erfahrungen gesammelt im Umgang mit Gamelab, die uns hoffentlich später nützen werden.

### Montag, der 10.09.2018
Heute haben wir es uns zur Aufgabe gemacht den vorhandenen Code zu organisieren und zu ordnen so gut es geht, um auf der einen Seite die Programmierung anschaulich und verständlich zu machen, aber auch um uns selber die spätere Arbeit zu erleichtern.
  (Vorher, Nachher Bilder????)
Zusätzlich dazu hatten wir noch Zeit zwei weitere Sprites zu erstellen. Der Eine sollte als zweite Charakter neben dem Elch dienen und heißt "nini". Als Animation haben wir vorerst ein Foto von Adriana genutzt. Der Andere wurde über die Sonne gesetzt und bestand aus einem Foto von Tim und heißt auch "Tim". Letztere diente überwiegend unserem eigenen Vergnügen und sollte eine Anspielung an die "Teletubbies" sein.
  (Bilder!!!)

### Dienstag, der 11.09.2018
Das Dauerthema "Sprung" hat uns auch heute wieder beschäftigt, jedoch nicht allzu sehr. Im fokus stand heute ein zweiter "ground", um das Spiel interessant zu halten. Dieser befindet sich auf der gleichen Y-Koordinate wie der erste Ground, jedoch immer auf der X-Achse 200 Einheiten weiter. Um das Prinzip "jump 'n Run" zu erhalten, haben wir beide Grounds so programmiert, dass diese sobald sie aus dem Sichtfeld des Spielers verschwinden wieder rechts neben dem anderen Block spawnen. So ist das Spiel nun auch praktisch open-end.

### Montag, der 17.09.2018
In der heutigen Stunde haben wir aus verschiedenen Gründen nicht viel geschafft. Der heute Fortschritt bestand lediglich aus einer Option für uns mit der Taste "A" aus dem Spiel herauszuzoomen, um einen besseren Überblick zu erhalten, insbesondere in der Hinsicht auf die immer wieder neu spawnenden "grounds".

### Dienstag, der 18.09.2018
Das bisherige Konzept eomes "Jump 'n Rums
- Konzept "Smuush"
- Festsetzung der Kamera 
- Festsetzen Ground 
- neue Steuerung nini "wasd"
- Marcel Davis für Elch 

### Montag, der 22.10.2018

- Siegerbildschirm "Marcel won, Nini won" 
- Sprungüberarbeitung für beide 
- Todesursachen für beide 

### Montag, der 29.10.2018


### Dienstag, der 30.10.2018


### Dienstag, der 06.11.2018


### Montag, der 12.11.2018
Heute haben wir es endlich geschafft den Sprung zu optimieren. Geholfen haben uns dabei die Gamelab-eigenen Tutorials, die wir bis zu dem Zeitpunkt bewusst völlig außer Acht gelassen hatten. Für einen natürlich wirkenden Sprung haben wir uns unseren Wissens über die Physik bedient: Einer nach oben wirkenden Geschwindigkeit wirkt eine nach unten gerichtete Beschleunigung entgegen. Zuerst wollten wir als Beschleunigung den Wert 9,81 nutzen. Dieser hat sich leider als nicht praktisch erwiesen und zu hoch erwiesen. Deswegen beträgt er jetzt nur noch den Wert 2.

### Dienstag, der 13.11.2018
Für ein interessanteres Spiel haben wir den "ground2" höher gesetzt und damit das "spielfeld" vergrößert". Dementsprechend mussten wir auch die Sprunghöhe, sprich die Ausgangsgeschwindigkeit des Sprungs, für die Sprites anpassen. Heute entstand auch die erste Form eines Startmenüs. Dies bestand zunächst nur aus dem Text "start" vor einem hellblauen Hintergrund. Der Hintergrund war in Wirklichkeit auch der Hintergrund des Spiels, nur haben wir für das Startmenü sehr weit hereingezoomt. Um das Spiel zu "starten" musste man "1" drücken. Daraufhin wurde wieder herausgezoomt, der Text verschwand und man konnte spielen. (BILD) Auch das Thema "Kräftegleichgewicht" zwischen den beiden Sprites hat uns heute wieder beschäftigt. Leider sind wir noch zu keinern
- Erhöhung "ground2" 
  - dementsprechende Anpassung der Sprunghöhe 
- Text "start" Konfig 
- Arbeiten am Kräftegleichgewicht Nini und marci 

