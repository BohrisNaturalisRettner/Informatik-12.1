# "Smooosh" - Arbeitsprotokoll 
von David Rettmann und Tim Wähner                                                                              
Stormarnschule Ahrensburg                                                                         
Klasse 12e                                                                                
Schuljahr 18/19                                                                                                   

## Inhalt

### August
[Dienstag, der 21.08.2018](#1)                         
[Montag, der 27.08.2018](#2)                         
[Dienstag, der 28.08.2018](#3)  

### September
[Sonntag, der 02.09.2018](#4)                        
[Montag, der 03.09.2018](#5)                    
[Samstag, der 08.09.2018](#6)                         
[Sonntag, der 09.09.2018](#7)                
[Montag, der 10.09.2018](#8)                                  
[Dienstag, der 11.09.2018](#9)                                          
[Montag, der 17.09.2018](#10)                                                   
[Dienstag, der 18.09.2018](#11) 

### Oktober
[Montag, der 22.10.2018](#12)                                           
[Montag, der 29.10.2018](#13)                                            
[Dienstag, der 30.10.2018](#14)  

### November
[Dienstag, der 06.11.2018](#15)                                        
[Montag, der 12.11.2018](#16)                                             
[Dienstag, der 13.11.2018](#17)                                                                 
[Mittwoch, der 14.11.2018](#18)                                                                                       
[Freitag, der 16.11.2018](#19)                                                                                          
[Samstag, der 17.11.2018](#20)                                                                                               
[Montag, der 19.11.2018](#21)                                                                                         
[Dienstag, der 20.11.2018](#22)                                                                                     
[Mittwoch, der 21.11.2018](#23)                                                                                        
[Donnerstag, der 22.11.2018](#24)                                                                                  
[Freitag, der 23.11.2018](#25)                                                                                          

### Dienstag, der 21.08.2018<a name="1"></a>

In der ersten Doppelstunde Informatik gab Herr Buhl uns zunächst eine kleine Einführung und erläuterte das Vorgehen im nächsten Schuljahr. Daraufhin hatten wir etwas Zeit uns mit seiner eigenen Seite zum Thema <a href="https://github.com/jbuhl/InformatikUnterricht">"Wege durch den Informatikunterricht mit Herrn Buhl"<a/> zu beschäftigen. Auf dieser konnten wir uns mit einigen möglichen Programmen auseinandersetzen, was wir auch fleißig taten. Für uns standen zunächst auf Grund unser sehr eingeschränkten Erfahrungen im Programmieren, Greenfoot und Applab im Fokus.

### Montag, der 27.08.2018<a name="2"></a>

Heute haben wir uns mit den beiden Programmen näher auseinandergesetzt, die gestern für uns geeignet erschienen und sind gemeinsam zu dem Schluss gekommen, dass wir lieber mit Applab als mit Greenfoot arbeiten würden. Bei Applab gefiel uns zum einen die Art und Weise mit der man Buttons und Slider einfügen und verwenden konnte und zum anderen die Vielzahl an Möglichkeiten die verschiedenen Screens zu gestalten. Mit den Buttons haben wir auch schon erste kleine Funktionen verbunden, wie zum Beispiel die "Turtle" auf dem Screen herumzubewegen.

<img src="https://github.com/BohrisNaturalisRettner/ToDo/blob/master/turtle%20beispiel%20protokoll.png" alt="image" width="500"> 

### Dienstag, der 28.08.2018<a name="3"></a>

Während unserer Arbeit auf Applab, haben wir auf der seite <a href="https://studio.code.org/projects/public">"code.org"<a/> auch Gamelab entdeckt. Gamelab ist im Gegensatz zu Applab, wie der Name schon sagt, tendenziell besser für die Programmierung eines Spiels geeignet, durch die mögliche Erstellung von Sprites. Nun standen wir erneut vor einer Entscheidung, haben uns jedoch schnell für die Programmierung eines Spiels entschieden. So nutzten wir die restliche Zeit in dieser Doppelstunde um uns mit Gamelab vertraut zu machen. 

### Sonntag, der 02.09.2018<a name="4"></a>

Auch außerhalb des Unterrichts haben wir uns mit Informatik beschäftigt. An diesem Sonntag entstand unser erstes richtiges Konzept. Das Spiel sollte ein "Jump 'n Run" werden. Wir begannen auch direkt mit der Umsetzung. Zunächst erstellten wir den Hintergrund, eine Sonne, einen ersten Untergrund und einen Stein. 

<img src="https://github.com/BohrisNaturalisRettner/ToDo/blob/master/Screenshot%20(34).png" alt="image" width="500"> 

Als "Spielfigur" sollte ein Sprite dienen, für den wir eine Animation von Gamelab nutzten, die einen Elch darstellte. Dieser sollte natürlich auch steuerbar sein. Die Steuerung setzten wir mit "if-Klauseln" auf die Pfeiltasten. 

```
function draw() {
  if (keyDown("left")) {
    elk.x = elk.x-10;
  }
  if (keyDown("right")) {
    elk.x = elk.x+10;
  }
  if (keyDown("up")) {
    playSound("sound://category_digital/hop.mp3", false);
    elk.velocityY = -10;
  } else {
    elk.velocityY = 10;
  }
  if (keyDown("down")) {
    elk.y = elk.y+10;
  }
  drawSprites();
```
Als erstes Feature programmierten wir, dass der Elch stirbt, sobald er herunterfällt oder die Sonne berührt. Geschieht dies erscheint eine "Todesnachricht" (Wasted) und man hört einen Sound. 

```
if (elk.x - ground2.x > 400) {
    ground2.x = elk.x + 400;
  }
  if (ground2.x - elk.x > 400) {
    ground2.x = elk.x - 400;
  }
  if (elk.isTouching(sun)) {
    wasted.visible = 100;
    playSound("sound://category_background/jazzy_beats.mp3", false);
    stopSound("sound://category_background/repitition.mp3");
    stopSound("sound://category_background/progression.mp3");
    elk.setFrame(1);
    elk.setVelocity(0, 0);
  } else {
    elk.setFrame(0);
  }
  if (elk.y > 400) {
    elk.destroy();
    wasted.visible = 100;
    playSound("sound://category_background/jazzy_beats.mp3", false);
    stopSound("sound://category_background/repitition.mp3");
    stopSound("sound://category_background/progression.mp3");
    
  }
}
drawSprites();
```


### Montag, der 03.09.2018<a name="5"></a>

In der heutigen Stunde haben wir uns eigentlich vorgenommen den Sprung natürlicher und realistischer aussehen zu lassen, jedoch ist es uns trotz unserer Bemühungen nicht gelungen. 

### Samstag, der 08.09.2018<a name="6"></a>

Um das Spiel insgesamt flüssiger scheinen zu lassen, haben wir heute die Kamera auf den Sprite "Elch" fixiert. Dies führt dazu, dass nun der "Elch" im ständigen Mittelpunkt des Spiels befindet und sich der Hintergrund und die Böden ihm "hinterherbewegen". Dadurch haben wir das Spiel auf der horizontalen Ebene theoretisch "open end". 

```
  back.x = elk.x;
  back.y = elk.y - 69;
  camera.x = elk.x;
  camera.y = elk.y - 69;
```


### Sonntag, der 09.09.2018<a name="7"></a>

Dadurch, dass wir am letzten Montag am Sprung erneut gescheitert sind, haben wir uns heute noch einmal an diese Thematik herangewagt, sind leider jedoch wieder "gescheitert". Trotzdem haben wir weitere Erfahrungen gesammelt im Umgang mit Gamelab, die uns hoffentlich später nützen werden.

### Montag, der 10.09.2018<a name="8"></a>

Heute haben wir es uns zur Aufgabe gemacht den vorhandenen Code zu organisieren und zu ordnen so gut es geht, um auf der einen Seite die Programmierung anschaulich und verständlich zu machen, aber auch um uns selber die spätere Arbeit zu erleichtern.
  (Vorher, Nachher Bilder????)
Zusätzlich dazu hatten wir noch Zeit zwei weitere Sprites zu erstellen. Der Eine sollte als zweite Charakter neben dem Elch dienen und heißt "nini". Als Animation haben wir vorerst ein Foto von Adriana genutzt. Der Andere wurde über die Sonne gesetzt und bestand aus einem Foto von Tim und heißt auch "Tim". 

### Dienstag, der 11.09.2018<a name="9"></a>

Das Dauerthema "Sprung" hat uns auch heute wieder beschäftigt, jedoch nicht allzu sehr. Im fokus stand heute ein zweiter "ground", um das Spiel interessant zu halten. Dieser befindet sich auf der gleichen Y-Koordinate wie der erste Ground, jedoch immer auf der X-Achse 200 Einheiten weiter. Um das Prinzip "jump 'n Run" zu erhalten, haben wir beide Grounds so programmiert, dass diese sobald sie aus dem Sichtfeld des Spielers verschwinden wieder rechts neben dem anderen Block spawnen. So ist das Spiel nun auch praktisch open-end.

```
 if (elk.x - ground2.x > 400) {
    ground2.x = elk.x + 400;
  }
  if (ground2.x - elk.x > 400) {
    ground2.x = elk.x - 400;
```

### Montag, der 17.09.2018<a name="10"></a>

In der heutigen Stunde haben wir aus verschiedenen Gründen nicht viel geschafft. Der heute Fortschritt bestand lediglich aus einer Option für uns mit der Taste "A" aus dem Spiel herauszuzoomen, um einen besseren Überblick zu erhalten, insbesondere in der Hinsicht auf die immer wieder neu spawnenden "grounds".

``` 
if (keyDown("a")) {
    camera.zoom = 0.3;
  } else {
    camera.zoom = 0.5;
```

### Dienstag, der 18.09.2018<a name="11"></a>

Das bisherige Konzept eines "Jump 'n Runs" ist mehr oder minder aus der Unschlüssigkeit heraus entstanden, hat uns aber nie so erfüllt wie wir es uns gewünscht haben. Deswegen waren wir auch beide sofort bereit, unser bisheriges Konzept aufzugeben und auf ein anderes umzuschwenken. Wir haben schon in den letzten Stunden herumgescherzt, man könne anstelle eines "Jump 'n Runs" sich am Spiel "Super Smash Bros." orientieren, dessen Spielprinzip übernehmen und auf eigene Weise umsetzen. Unser Spiel sollte nun, in Anlehnung an "smash", "smooosh" heißen. Erster Schritt dafür war die Festsetzung der Kamera, des Hintergrunds und der grounds. Nun bewegten sich der "Elch" und "nini" wieder im Vordergrund. Für "nini" haben wir die Steuerung auf die Tasten "W","A","S" und "D" gelegt. Außerdem haben wir die Animation des Elchs entfernt und stattdessen das Gesicht von Marcel Davis genutzt. 

### Montag, der 22.10.2018<a name="12"></a>

Dadurch das es jetzt immer einen Sieger und einen Verlierer geben sollte, haben wir zunächst die Todesursache im Spiel festgelegt. Sobald einer der Sprites sich auf der Y-Achse über dem Wert 360 befinden, erscheint der Siegerbildschirm für den anderen Spieler, sprich entweder "Marcel won" oder "Nini won". (SCREENSHOTS)

### Montag, der 29.10.2018<a name="13"></a>

Für ein interessanteres Spiel haben wir den "ground2" höher gesetzt und damit das "Spielfeld" vergrößert". Dementsprechend mussten wir auch die Sprunghöhe, sprich die Ausgangsgeschwindigkeit des Sprungs, für die Sprites anpassen. Heute entstand auch die erste Form eines Startmenüs. Dies bestand zunächst nur aus dem Text "start" vor einem hellblauen Hintergrund. Der Hintergrund war in Wirklichkeit auch der Hintergrund des Spiels, nur haben wir für das Startmenü sehr weit hereingezoomt. Um das Spiel zu "starten" musste man "1" drücken. Daraufhin wurde wieder herausgezoomt, der Text verschwand und man konnte spielen. (BILD) Auch das Thema "Kräftegleichgewicht" zwischen den beiden Sprites hat uns heute wieder beschäftigt, jedoch ohen ein nennenswertes Ergebnis.

### Dienstag, der 30.10.2018<a name="14"></a>

Heute haben wir es endlich geschafft den Sprung zu optimieren. Geholfen haben uns dabei die Gamelab-eigenen Tutorials, die wir bis zu dem Zeitpunkt bewusst völlig außer Acht gelassen hatten. Für einen natürlich wirkenden Sprung haben wir uns unseren Wissens über die Physik bedient: Einer nach oben wirkenden Geschwindigkeit wirkt eine nach unten gerichtete Beschleunigung entgegen. Zuerst wollten wir als Beschleunigung den Wert 9,81 nutzen, welcher sich jedoch als eindeutig zu hoch erwiesen hat. Deswegen beträgt der Wert jetzt nur noch eins. 

```
} if (keyWentDown("up")) {
      elk.velocityY = -15;
```

In dem Code oben befindet sich die Steuerung für den Sprung von Spieler 2. Drückt er die Taste "up", so bekommt der Charakter eine nach obene gerichtete Geschwindigkeit mit dem Wert 15. Dieser Geschwindigkeit wirkt die generelle Beschleunigung, die im Code für den Schub nach unten verankert ist.

```
if (keyDown("down")) {
      elk.velocityY = elk.velocityY+10;
    } else {
      elk.velocityY = elk.velocityY + 1;
```

### Dienstag, der 06.11.2018<a name="15"></a>

Die heutige Doppelstunde haben wir einzig und allein Github gewidmet. Zum einen mussten wir unser Arbeitsprotokoll bearbeiten und in Reinform bringen und zum anderen an der Projektseite arbeiten, um am Ende der Zeit nicht in Stress zu verfallen. 

### Montag, der 12.11.2018<a name="16"></a>

Die Ordnung ist erneut ein Thema, das unserer Aufmerksamkeit bedarf. Nach vielen Veränderungen, die wir auch zum Teil spontan an verschiedenen Stellen des Codes vorgenommen haben, ist es mal wieder Zeit uns selber die Arbeit zu erleichtern und die Commands zu sortieren. Wie schon bereits am [Montag, dem 10.09.2018](#8) galt es ähnliche Commands zusammenzuordnen. 

### Dienstag, der 13.11.2018<a name="17"></a>

Im Sinne unseres neuen Konzepts haben wir heute auch eine dritte Plattform programmiert. Diese und die zweite Plattform sollen sich auch bewegen und in gewissem Maße an zufälligen Orten spawnen. 
```
function grounds() {
  if (mouseDown("leftButton")&&(player2.visible===true||ground.visible===true)) {
    ground2.velocityX = -0.5;
    ground3.velocityY = -0.5;
  }
  if ((ground2.x==50 && ground2.velocityX < 0)) {
    ground2.velocityX = 0.5;
  }
  if ((ground3.y)<=200 && ground3.velocityY < 0) {
    ground3.velocityY = 0.5;
  }
  if ((ground2.x==200 && ground2.velocityX > 0)) {
     ground2.velocityX = -0.5;
  }
  if (ground3.y>=350 && ground3.velocityY > 0) {
    ground3.velocityY = -0.5;
  }
}
```
In diesem Code wurde zuerst festgelegt, dass der Spieler 2 einen Charakter ausgewählt haben muss, um die anderen Aktionen ins Rollen zu bringen. Ground 2 bekommt eine Geschwindigkeit in X-Richtung und Ground 3 eine Geschwindigkeit in Y-Richtung. Sobald sie auf ihrer Route einen gewissen Punkt überschritten haben bekommen sie eine entgegengesetzte Geschwindigkeit und machen sich auf den "Rückweg". So geht das theoretisch ewig hin und her.                                                                                  
Im folgenden Code ist beschrieben, dass zum Beispiel Ground 1 seinen Mittelpunkt auf einem zufälligen Punkt auf der X-Achse zwischen 120 und 130 hat. Danach ist auch die Größe der PLattform vorgegeben mit 50 in der Höhe und 120 in der Breite.

```
//ground1
var ground = createSprite(randomNumber(120, 130), 350);
ground.setAnimation("Wolke");
ground.height = 50;
ground.width = 120;
//ground2
var ground2 = (createSprite(randomNumber(100, 200), 200));
ground2.setAnimation("Wolke");
ground2.scale = 0.3;
//ground3
var ground3 = createSprite(ground.x+170, ground.y-randomNumber(30,70));
ground3.setAnimation("Wolke");
ground3.height = 30;
ground3.width = 100;
```
 
### Mittwoch, der 14.11.2018<a name="18"></a>

Heute haben wir uns den Variablen gewidmet. Bei ein paar öffentlichen Projekten haben wir gesehen, dass sie eine große Rolle spielen können und viele neue Funktionen ermöglichen. Also haben wir anhand von Versuchen mit den anderen Spielen als grobe Vorlage innerhalb und außerhalb des Hauptprojekts die Funktionsweise von Variablen erarbeitet und weiter erschlossen.


### Freitag, der 16.11.2018<a name="19"></a>

Wir hielten es, vor allem auch auf Grund der unzuverlässigen Kollisionen in Gamelab, für notwendig, dass die Spieler unseres Spiels neben dem Herunterschubsen auch eine andere Möglichkeit haben den Gegner zu bezwingen. Für uns erschien eine Art Projektil logisch. So machten wir uns Gedanken und landeten schließlich mit Hilfe des vorgestern angeeigenten Wissens über Variablen bei diesem Code:

```
function projectiles() {
  if (keyWentDown("q")&&q>50&&nini.visible===true) {
          projectile1.x = nini.x;
          projectile1.y = nini.y;
          projectile1.visible = true;
          projectile1.velocityX = -7;
          q = 0;
    } else if ((keyWentDown("e")&&e>50&&nini.visible===true)) {
        projectile2.x = nini.x;
        projectile2.y = nini.y;
        projectile2.visible = true;
        projectile2.velocityX = 7;
        e = 0;
    } else if (keyWentDown("alt")&&alt>50&&elk.visible===true) {
        projectile3.x = elk.x;
        projectile3.y = elk.y;
        projectile3.visible = true;
        projectile3.velocityX = -7;
        alt = 0;
    } else if (keyWentDown("shift")&&shift>50&&elk.visible===true) {
        projectile4.x = elk.x;
        projectile4.y = elk.y;
        projectile4.visible = true;
        projectile4.velocityX = 7;
        shift = 0;
     }
  if (projectile1.isTouching(edges)) {
    projectile1.visible = false;
  }
  if (projectile2.isTouching(edges)) {
    projectile2.visible = false;
  }
  if (projectile3.isTouching(edges)) {
    projectile3.visible = false;
  }
  if (projectile4.isTouching(edges)) {
    projectile4.visible = false;
  }
}
```

### Samstag, der 17.11.2018<a name="20"></a>

Ein weiterer Aspekt den wir an dem Projekt ändern mussten, um mehr Möglichkeiten zu haben war die Einführung von weiteren Funktionen als der Function(draw). Wir haben uns daraufhin mit diesem Thema auseinandergesetzt und die Funktionsweise von Funktionen besser verstanden. Daraufhin haben wir auch für früher erstellte Abläufe Funktionen angelegt. Dies bot zum einen eine bessere Übersicht zum anderen konnte man so viel leichter Abhängigkeiten verschiedener Abläufe festlegen.


### Montag, der 19.11.2018<a name="21"></a>
Die neuen Entdeckungen haben uns sehr begeistert. Nachdem wir vorher ein wenig im Projekt festgefahren waren hat sind wir jetzt sehr motiviert unser Projekt zu verbessern. Dafür haben wir mehrere Ideen die wir bis zur Abgabe noch umsetzen wollten. Als erstes wollten wir einen Startbildschirm designen und es wie in "Smash" ermöglichen, sich vor dem Spiel seinen Charakter auszusuchen. Nach einiger Zeit haben wir aber gemerkt, dass sich die Umsetzung eines solchen Plans doch schwerer war als erwartet. Daraufhin haben wir uns dem Todesszenario zugewendet und die Umsetzung der Spielerauswahl erstmal aufgeschoben. Wir wollten eine Umsetzung der Tode, ohne, dass man das Programm an sich neu starten muss. Innerhalb einer neuen function(death) haben wir unsere Vorstellungen umgesetzt. 


function death() {
  if (nini.y >= 360) {
    pup = 0;
    pup3e = 0;
    fill(rgb(0, 0, 0));
    text("Player 1 died", 110, 150);
    if (nini.visible===true) {
      nini.visible=false;
      scoreelk = scoreelk+1;
    }
    if (nini.visible===false) {
      dnini = dnini+1;
      if (dnini>30) {
        elk.visible=true;
        nini.visible=true;
        start1.visible = true;
        start2.visible = true;
        nini.x=start1.x;
        nini.y=start1.y-40;
        elk.x=start2.x;
        elk.y=start2.y-40;
        dnini = 0;
      }
    }
  } else if (elk.y >= 360) {
    pup = 0;
    pup3n = 0;
    fill(rgb(0, 0, 0));
    text("Player 2 died", 110, 150);
    if (elk.visible === true) {
      elk.visible=false;
      scorenini = scorenini+1;
    }
    if (elk.visible===false) {
      delk = delk+1;
      if (delk>30) {
        elk.visible=true;
        nini.visible=true;
        start1.visible = true;
        start2.visible = true;
        nini.x=start1.x;
        nini.y=start1.y-40;
        elk.x=start2.x;
        elk.y=start2.y-40;
        delk = 0;
      }
    }
  }
  fill(rgb(255, 255, 255));
  rect(219, 0, 180, 70);
  fill(rgb(0, 0, 0));
  text("Spieler 2: "+scoreelk, 225, 60);
  text("Spieler 1: "+scorenini, 225, 30);
  drawSprites();
  if (keyDown("0")) {
    scorenini = 0;
    scoreelk = 0;
  }
  if (elk.x<320) {
    start2.visible = false;
  }
  if (nini.x>80) {
    start1.visible = false;
  }
  drawSprites();
}


### 14-19 November 2018
- Scoreboard
- Respawn
- Startmenü
- Anpassung des Wegrutschens 
- Flugzeug 
- Powerup

### Dienstag, der 20.11.2018<a name="22"></a>


-
### Mittwoch, der 21.11.2018<a name="23"></a>



### Donnerstag, der 22.11.2018<a name="24"></a>#



### Freitag, der 23.11.2018<a name="25"></a>
Heute haben wir die letzen kleinen Änderungen am Projekt vorgenommen und sowohl die Projektseite als auch das Arbeitsprotokoll fertiggestellt.
