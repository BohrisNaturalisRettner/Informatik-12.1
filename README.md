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

In der ersten Doppelstunde Informatik nach den Sommerferien gab Herr Buhl uns zunächst eine kleine Einführung und erläuterte das Vorgehen im nächsten Schuljahr. Daraufhin hatten wir etwas Zeit, uns mit seiner eigenen Seite zum Thema <a href="https://github.com/jbuhl/InformatikUnterricht">"Wege durch den Informatikunterricht mit Herrn Buhl"<a/> zu beschäftigen. Auf dieser konnten wir uns mit einigen möglichen Programmen auseinandersetzen, was wir auch fleißig taten. Für uns standen zunächst aufgrund unser sehr eingeschränkten Erfahrungen im Programmieren Greenfoot und Applab im Fokus.

### Montag, der 27.08.2018<a name="2"></a>

Heute haben wir uns mit den beiden Programmen näher auseinandergesetzt, die uns nach unseren bisherigen Erfahrungen als geeignet erschienen und sind gemeinsam zu dem Schluss gekommen, dass wir lieber mit Applab als mit Greenfoot arbeiten würden. Bei Applab gefiel uns zum einen die Art und Weise, mit der man Buttons und Slider einfügen und verwenden konnte und zum anderen die Vielzahl an Möglichkeiten, die verschiedenen Screens zu gestalten. Mit den Buttons haben wir auch schon erste kleine Funktionen verbunden, wie zum Beispiel die "Turtle" auf dem Screen herumzubewegen.

<img src="https://github.com/BohrisNaturalisRettner/ToDo/blob/master/turtle%20beispiel%20protokoll.png" alt="image" width="500"> 

<img scr="Bildschirmfoto 2018-11-23 um 22.59.43.png" alt="image" width="500">




<img scr="Bildschirmfoto 2018-11-23 um 23.28.48.png" alt="image" width="500">




<img scr="Bildschirmfoto 2018-11-23 um 23.29.49.png" alt="image" width="500">






<img scr="Bildschirmfoto 2018-11-23 um 23.31.27.png" alt="image" width="500">





<img scr="Bildschirmfoto 2018-11-23 um 23.36.13.png" alt="image" width="500">





<img scr="Bildschirmfoto 2018-11-23 um 23.37.29.png" alt="image" width="500">






<img scr="Bildschirmfoto 2018-11-23 um 23.40.01.png" alt="image" width="500">

### Dienstag, der 28.08.2018<a name="3"></a>

Während unserer Arbeit auf Applab haben wir auf der Seite <a href="https://studio.code.org/projects/public">"code.org"<a/> auch Gamelab entdeckt. Gamelab ist im Gegensatz zu Applab, wie der Name schon sagt, tendenziell besser für die Programmierung eines Spiels geeignet, und zwar wegen der Möglichkeit, Sprites zu erstellen. Nun standen wir erneut vor einer Entscheidung, haben uns jedoch schnell für die Programmierung eines Spiels entschieden. Die restliche Zeit in dieser Doppelstunde nutzten wir, um uns mit Gamelab vertraut zu machen. 

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

Für die heutige Stunde hatten wir uns vorgenommen, den Sprung natürlicher und realistischer aussehen zu lassen, was uns jedoch trotz intensiver Bemühungen nicht gelungen ist. 

### Samstag, der 08.09.2018<a name="6"></a>

Um das Spiel insgesamt flüssiger scheinen zu lassen, haben wir heute die Kamera auf den Sprite "Elch" fixiert. Dies führt dazu, dass sich der "Elch" nun im ständigen Mittelpunkt des Spiels befindet und sich der Hintergrund und die Böden "hinter ihm herbewegen". Dadurch haben wir das Spiel auf der horizontalen Ebene theoretisch "open end" gestaltet. 

```
  back.x = elk.x;
  back.y = elk.y - 69;
  camera.x = elk.x;
  camera.y = elk.y - 69;
```


### Sonntag, der 09.09.2018<a name="7"></a>

Weil wir am letzten Montag am Sprung erneut gescheitert waren, haben wir uns heute noch einmal an diese Thematik herangewagt, waren jedoch leider wieder nicht erfolgreich. Trotzdem haben wir weitere Erfahrungen gesammelt im Umgang mit Gamelab, die uns hoffentlich später nützen werden.

### Montag, der 10.09.2018<a name="8"></a>

Heute haben wir es uns zur Aufgabe gemacht, den vorhandenen Code, so gut es geht, zu organisieren und zu ordnen, um auf der einen Seite die Programmierung anschaulich und verständlich zu machen, aber auch, um uns selbst die spätere Arbeit zu erleichtern.
Ergänzend hatten wir noch Zeit, zwei weitere Sprites zu erstellen. Der eine sollte als zweiter Charakter neben dem Elch dienen - wir haben ihn "nini" getauft. Als Animation haben wir vorerst ein Foto von Adriana genutzt. Der andere wurde über die Sonne gesetzt und bestand aus einem Foto von Tim, weshalb wir ihn auch "Tim" genannt haben. 

### Dienstag, der 11.09.2018<a name="9"></a>

Das Dauerthema "Sprung" hat uns auch heute wieder beschäftigt, jedoch nicht so stark, wie in den Wochen zuvor. Im Fokus stand heute ein zweiter "ground", um das Spiel interessant zu halten. Dieser befindet sich auf der gleichen Y-Koordinate wie der erste Ground, jedoch auf der X-Achse stets 200 Einheiten weiter. Um das Prinzip "jump 'n Run" zu erhalten, haben wir beide Grounds so programmiert, dass diese, sobald sie aus dem Sichtfeld des Spielers verschwunden waren, wieder rechts neben dem anderen Block spawnen. So ließ sich das Spiel nun auch praktisch open-end spielen.

```
 if (elk.x - ground2.x > 400) {
    ground2.x = elk.x + 400;
  }
  if (ground2.x - elk.x > 400) {
    ground2.x = elk.x - 400;
```

### Montag, der 17.09.2018<a name="10"></a>

In der heutigen Stunde haben wir aus verschiedenen Gründen nicht viel geschafft. Der heutige Fortschritt bestand lediglich aus einer Option für uns, mit der Taste "A" aus dem Spiel herauszuzoomen, um einen besseren Überblick zu erhalten, insbesondere in der Hinsicht auf die immer wieder neu spawnenden "grounds".

``` 
if (keyDown("a")) {
    camera.zoom = 0.3;
  } else {
    camera.zoom = 0.5;
```

### Dienstag, der 18.09.2018<a name="11"></a>

Wir haben festgestellt, dass uns unser bisheriges Konzept eines "Jump 'n Runs" nicht so überzeugt, wie wir es uns gewünscht haben. Deswegen waren wir auch beide sofort bereit, unser bisheriges Konzept aufzugeben und auf ein anderes umzuschwenken, als uns hierfür eine gute Idee kam. Wir hatten schon in den letzten Stunden herumgescherzt, man könne sich anstelle eines "Jump 'n Runs" besser am Spiel "Super Smash Bros." orientieren, dessen Spielprinzip übernehmen und auf eigene Weise umsetzen. Unser Spiel sollte nun, in Anlehnung an "smash", "smooosh" heißen. Erster Schritt dafür war die Festsetzung der Kamera, des Hintergrunds und der grounds. Nun bewegten sich der "Elch" und "nini" wieder im Vordergrund. Für "nini" haben wir die Steuerung auf die Tasten "W","A","S" und "D" gelegt. Außerdem haben wir die Animation des Elchs entfernt und stattdessen das Gesicht von Marcel Davis genutzt. 

### Montag, der 22.10.2018<a name="12"></a>

Weil es nach unserer neuen Spielidee immer einen Sieger und einen Verlierer geben sollte, haben wir zunächst die Todesursache im Spiel festgelegt. Sobald einer der Sprites sich auf der Y-Achse über dem Wert 360 befinden, erscheint der Siegerbildschirm für den anderen Spieler, sprich entweder "Marcel won" oder "Nini won". (SCREENSHOTS)

### Montag, der 29.10.2018<a name="13"></a>

Für ein interessanteres Spiel haben wir den "ground2" höher gesetzt und damit das "Spielfeld" vergrößert". Dementsprechend mussten wir auch die Sprunghöhe, sprich die Ausgangsgeschwindigkeit des Sprungs für die Sprites anpassen. Heute entstand auch die erste Form eines Startmenüs. Dies bestand zunächst nur aus dem Text "start" vor einem hellblauen Hintergrund. Der Hintergrund war in Wirklichkeit auch der Hintergrund des Spiels, nur haben wir für das Startmenü sehr weit hereingezoomt. Um das Spiel zu "starten" musste man "1" drücken. Daraufhin wurde wieder herausgezoomt, der Text verschwand und man konnte spielen. Auch das Thema "Kräftegleichgewicht" zwischen den beiden Sprites hat uns heute wieder beschäftigt, jedoch ohne ein nennenswertes Ergebnis.

### Dienstag, der 30.10.2018<a name="14"></a>

Heute haben wir es endlich geschafft, den Sprung zu optimieren. Geholfen haben uns dabei die Gamelab-eigenen Tutorials. Für einen natürlich wirkenden Sprung haben wir uns unseren Wissens über die Physik bedient: Einer nach oben wirkenden Geschwindigkeit wirkt eine nach unten gerichtete Beschleunigung entgegen. Zuerst wollten wir als Beschleunigung den Wert 9,81 nutzen, welcher sich jedoch als eindeutig zu hoch erwiesen hat. Deswegen beträgt der Wert jetzt nur noch eins. 

```
} if (keyWentDown("up")) {
      elk.velocityY = -15;
```

In dem Code oben befindet sich die Steuerung für den Sprung von Spieler 2. Drückt er die Taste "up", so bekommt der Charakter eine nach oben gerichtete Geschwindigkeit mit dem Wert 15. Dieser Geschwindigkeit wirkt die generelle Beschleunigung, die im Code für den Schub nach unten verankert ist.

```
if (keyDown("down")) {
      elk.velocityY = elk.velocityY+10;
    } else {
      elk.velocityY = elk.velocityY + 1;
```

### Dienstag, der 06.11.2018<a name="15"></a>

Die heutige Doppelstunde haben wir einzig und allein Github gewidmet. Zum einen mussten wir unser Arbeitsprotokoll bearbeiten und in Reinform bringen und zum anderen an der Projektseite arbeiten, um am Ende der Zeit nicht in Stress zu verfallen. 

### Montag, der 12.11.2018<a name="16"></a>

Die Ordnung ist erneut ein Thema, das unserer Aufmerksamkeit bedarf. Nach vielen Veränderungen, die wir auch zum Teil spontan an verschiedenen Stellen des Codes vorgenommen haben, ist es mal wieder Zeit, uns selber die Arbeit zu erleichtern und die Commands zu sortieren. Wie schon bereits am [Montag, dem 10.09.2018](#8) galt es, ähnliche Commands zusammenzuordnen. 

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
In diesem Code wurde zuerst festgelegt, dass der Spieler 2 einen Charakter ausgewählt haben muss, um die anderen Aktionen ins Rollen zu bringen. Ground 2 bekommt eine Geschwindigkeit in X-Richtung und Ground 3 eine Geschwindigkeit in Y-Richtung. Sobald sie auf ihrer Route einen gewissen Punkt überschritten haben, bekommen sie eine entgegengesetzte Geschwindigkeit und machen sich auf den "Rückweg". So geht das theoretisch ewig hin und her.                                                                                  
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

### Donnerstag, der 15.11.2018<a name="19"></a>

Wir haben uns weiter mit den Variablen beschäftigt und herumexperimentiert. Außerdem haben wir das Design überarbeitet. Aufgrund der schwebenden Plattformen, haben wir uns dafür entschieden Wolken anstelle der Böden zu benutzen.

### Freitag, der 16.11.2018<a name="20"></a>

Wir hielten es, vor allem auch auf Grund der unzuverlässigen Kollisionen in Gamelab, für notwendig, dass die Spieler unseres Spiels neben dem Herunterschubsen auch eine andere Möglichkeit haben, den Gegner zu bezwingen. Für uns erschien eine Art Projektil logisch. So machten wir uns Gedanken und landeten schließlich mit Hilfe des vorgestern und gestern angeeigenten Wissens über Variablen bei diesem Code:

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

### Freitag, der 16.11.2018<a name="21"></a>

Ein weiterer Aspekt, den wir an dem Projekt ändern mussten, um mehr Möglichkeiten zu haben, war die Einführung von weiteren Funktionen als der Function(draw). Wir haben uns daraufhin mit diesem Thema auseinandergesetzt und die Funktionsweise von Funktionen besser verstanden. Daraufhin haben wir auch für früher erstellte Abläufe Funktionen angelegt. Dies bot zum einen eine bessere Übersicht, zum anderen konnte man so viel leichter Abhängigkeiten verschiedener Abläufe festlegen.


### Samstag & Sonntag, 17 & 18.11.2018<a name="22"></a>
Die neuen Entdeckungen haben uns sehr begeistert. Nachdem wir vorher ein wenig im Projekt festgefahren waren, sind wir jetzt sehr motiviert, unser Projekt zu verbessern und haben an diesem Wochenende sehr intensiv gearbeitet. Dafür haben wir mehrere Ideen, die wir bis zur Abgabe noch umsetzen wollten. Als erstes wollten wir einen Startbildschirm designen und es wie in "Smash" ermöglichen, sich vor dem Spiel seinen Charakter auszusuchen. Nach einiger Zeit haben wir aber gemerkt, dass sich die Umsetzung eines solchen Plans doch schwerer war als erwartet. Daraufhin haben wir uns dem Todesszenario zugewendet und die Umsetzung der Spielerauswahl erstmal aufgeschoben. Wir wollten eine Umsetzung der Tode, ohne dass man das Programm an sich neu starten muss. Innerhalb einer neuen function(death) haben wir unsere Vorstellungen umgesetzt. Für einen Tod und Respawn, ohne das Spiel neu zu starten, erschien uns ein sprite.visible = false als sinnvoll. Die Sprites interagieren nach Einstellung nur, wenn sie sichtbar sind. Außerdem haben wir mit einer neuen Variable einen Timer eingestellt, nachdem die Spieler wieder sichtbar sind. Zusätzlich haben wir an einem Scoreboard gearbeitet, das bei dem Tod eines Spielers dem Gegenspieler einen Punkt gibt. Schwierig war es hierbei, zu erreiche, dass der Gegner nur einen Punkt erhält. Zusätzlich erscheint noch die Nachricht Player (1/2) died beim Todesfall. Jetzt sieht unsere function(death) so aus:



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
 

### Montag, der 19.11.2018<a name="23"></a>

Am Montag haben wir mit Hilfe von Variablen eine Begrenzung der Sprungmöglichkeiten der Charaktere eingeführt und dafür gesorgt, dass die Charaktere nicht mehr endlos springen können, sondern maximal einen Doppelsprung durch zweimaliges Klicken unternehmen können. 
Eine weitere Neuerung sind Startplattformen für die Spieler. 



### Dienstag, der 20.11.2018<a name="24"></a>
Heute haben wir zu Beginn unser Spiel erst selber gegeneinander gespielt, wobei uns ein Fehler aufgefallen ist, der bewirkte, dass sich die Spieler manchmal ohne das Drücken von Tasten auf den Plattformen bewegten und es auch sehr schwer war, gegen diese Geschwindigkeit "anzulaufen". Diesen Fehler haben wir dann mit dem einfachen Zusatz in der Movement Funktion behoben, dass, wenn keine Tasten gedrückt werden, die sprite.velocityX = 0 beträgt. 
```
} else {
      elk.velocityY = elk.velocityY + 1;
} else {
      nini.velocityY = nini.velocityY + 1;
```      
Weiterhin haben wir ein neues Konzept erstellt. Nach sehr intensiver Inspiration meiner (Davids) Mutter, haben wir uns entschlossen, noch ein Flugzeug in unser Spiel einzubauen, das in regelmäßigen Abständen durch den oberen Bildschirm fliegt. Die letztendliche Umsetzung gestaltete sich zunächst aber doch etwas schwieriger, weswegen wir das Projekt auf Morgen vertagen. 

### Mittwoch, der 21.11.2018<a name="25"></a>
Wie gestern schon erwähnt haben wir uns heute um die Verwirklichung des Traums meiner Mutter gekümmert, ein Flugzeug in das Spiel zu integrieren. Die Idee eines sinnlos umherfliegenden Flugzeuges hat uns aber nicht sehr begeistert. Nach einem Brain-storming, wie wir diese Idee sinnvoll umsetzen könnten, haben wir uns vorgenommen, ein Konzept umzusetzen, das wir schon lange im Hinterkopf hatten, das wir aber bislang als zu kompliziert empfundenden Konzept hatten. Das Flugzeug sollte an zufälligen Positionen powerups fallen lassen, die entweder dem eigenen Spieler besondere Fähigkeiten verschaffen oder den Gegner schwächen. Nach langem Herumprobieren sind wir fast an unserem Ziel angekommen. Das einzige Problem, das sich noch stellt, ist, dass das Flugzeug nicht bei Flug ein powerup fallen lässt, sondern nur bei manchen Flügen. Unsere powerups- und Flugzeugfunktionen sehen nun so aus:

```
function powerups() {
  if (flugzeug.x==abwurf) {
    pup2 = randomNumber(1, 6 );
    powerup.visible = true;
    powerup.x = flugzeug.x;
    powerup.y = flugzeug.y;
    powerup.velocityY = 1.5;
  }
  if (pup2===1) {
    powerup.setAnimation("powerupRed_bolt_1");
    if ((elk.isTouching(powerup)) && (powerup.visible===true)) {
      powerup.visible = false;
      pup3e=1;
    }
    if ((0<pup3e) && (pup3e<150) && (powerup.visible===false)) {
      nini.velocityY = nini.velocityY+10;
      pup3e = pup3e+1;
    }
    if (pup3e===150) {
      pup3e = 0;
      pup2 = 0;
    }
    if ((nini.isTouching(powerup)) &&(powerup.visible===true)) {
      powerup.visible = false;
      pup3n = 1;
    }
    if ((0<pup3n) && (pup3n<150) && (powerup.visible===false)) {
      elk.velocityY = elk.velocityY+10;
      pup3n = pup3n+1;
    }
    if (pup3n===150) {
      pup3n = 0;
    }
  }
  if (pup2===2) {
    powerup.setAnimation("powerupGreen_bolt_1");
    if (elk.isTouching(powerup) && (powerup.visible===true)) {
      powerup.visible = false;
      pup3e=1;
    }
    if ((0<pup3e) && (pup3e<150) && (powerup.visible===false)) {
      up = 0;
      pup3e = pup3e+1;
    }
    if (pup3e===150) {
      pup3e = 0;
      pup2 = 0;
    }
    if (nini.isTouching(powerup) && (powerup.visible===true)) {
      powerup.visible = false;
      pup3n = 1;
    }
    if ((0<pup3n) && (pup3n<150) && (powerup.visible===false)) {
      w = 0;
      pup3n = pup3n+1;
    }
    if (pup3n===150) {
      pup3n = 0;
    }
  }
  if (pup2===3) {
    powerup.setAnimation("powerupRed_shield_1");
    if (elk.isTouching(powerup) && (powerup.visible===true)) {
      powerup.visible = false;
      pup3e=1;
    }
    if ((0<pup3e) && (pup3e<150) && (powerup.visible===false)) {
      q = 0;
      e = 0;
      pup3e = pup3e+1;
    }
    if (pup3e===150) {
      pup3e = 0;
      pup2 = 0;
    }
    if (nini.isTouching(powerup)&& (powerup.visible===true)) {
      powerup.visible = false;
      pup3n = 1;
    }
    if ((0<pup3n) && (pup3n<150) && (powerup.visible===false)) {
      alt = 0;
      shift = 0;
      pup3n = pup3n+1;
    }
    if (pup3n===150) {
      pup3n = 0;
    }
  }
  if (pup2===4) {
    powerup.setAnimation("powerupGreen_shield_1");
    if (elk.isTouching(powerup)&& (powerup.visible===true)) {
      powerup.visible = false;
      pup3e=1;
    }
    if ((0<pup3e) && (pup3e<150) && (powerup.visible===false)) {
      projectile3.velocityX = -30;
      projectile4.velocityX = 30;
      if (projectile3.isTouching(nini)||projectile4.isTouching(nini)){
      nini.x = 300;
      nini.y = 380;
      }
      alt = 100;
      shift = 100;
      pup3e = pup3e+1;
    }
    if (pup3e===150) {
      pup3e = 0;
      pup2 = 0;
    }
    if (nini.isTouching(powerup)&& (powerup.visible===true)) {
      powerup.visible = false;
      pup3n = 1;
    }
    if ((0<pup3n) && (pup3n<150) && (powerup.visible===false)) {
      projectile1.velocityX = -30;
      projectile2.velocityX = 30;
      if (projectile1.isTouching(elk)||projectile1.isTouching(elk)){
      elk.x = 250;
      elk.y = 380;
      }
      q = 100;
      e = 100;
      pup3n = pup3n+1;
    }
    if (pup3n===150) {
      pup3n = 0;
    }
  }
  if (pup2===5) {
    powerup.setAnimation("powerupRed_star_1");
    if (elk.isTouching(powerup)&& (powerup.visible===true)) {
        powerup.visible = false;
        pup3e=1;
      }
    if (0<pup3e && pup3e<150 && powerup.visible===false) {
        pup3e = pup3e+1;
        nini.scale = 0.05;
      } else {
      nini.scale = 0.15;
    }
    if (pup3e===149) {
        pup3e = 0;
        pup2 = 0;
      }
    if (nini.isTouching(powerup)&& (powerup.visible===true)) {
        powerup.visible = false;
        pup3n = 1;
      }
    if (0<pup3n && pup3n<150 && powerup.visible===false) {
        pup3n = pup3n+1;
        elk.scale = 0.05;
      } else {
      elk.scale = 0.15;
    }
    if (pup3n===149) {
        pup3n = 0;
      }
  }
  if (pup2===6) {
    powerup.setAnimation("powerupGreen_star_1");
    if (elk.isTouching(powerup)&& (powerup.visible===true)) {
        powerup.visible = false;
        pup3e=1;
      }
    if (0<pup3e && (pup3e<150) && (powerup.visible===false)) {
        pup3e = pup3e+1;
        elk.scale = 0.3;
      } else {
      elk.scale = 0.15;
    }
    if (pup3e===150) {
        pup3e = 0;
        pup2 = 0;
      }
    if (nini.isTouching(powerup)&& (powerup.visible===true)) {
        powerup.visible = false;
        pup3n = 1;
      }
    if (0<pup3n && (pup3n<150) && (powerup.visible===false)) {
        pup3n = pup3n+1;
        nini.scale = 0.3;
      } else {
      nini.scale = 0.15;
    }
    if (pup3n===150) {
        pup3n = 0;
        pup2 = 0;
      }
  }
  }
  
 function jet() {
    if (f===500) {
    abwurf = randomNumber(100, 300);
    flugzeug.visible = true;
    flugzeug.velocityX = 3;
  }
    if (flugzeug.x>=450) {
    flugzeug.x=-100;
    flugzeug.velocityX = 0;
    flugzeug.visible = false;
    f = 0;
    drawSprites();
  }
}
```

### Donnerstag, der 22.11.2018<a name="26"></a>#
Das Projekt ist jetzt mit allen wichtigen Funktionen fertiggestellt. Zu guter Letzt haben wir uns dem Erstellen des Startbildschirmes und der Umsetzung der Spielerauswahlen gewidmet. Wie schon bei den powerups war hierfür viel Geduld und Probieren nötig, bis wir jetzt schlussendlich zu einem Ergebnis gekommen sind, das uns überzeugt. Auch wenn der Mausklick zum Auswählen der Spielers manchmal als Doppelklick gewertet wird und so der zweite Spieler gleich mit ausgewählt wird, funktionert es zumeist sehr zuverlässich und mit Maus sowieso bessser als mit dem Trackpad auf dem MacBook. Die Startfunktion des Spiels haben wir folgendermaßen gestaltet:


```
function button() {
  if (player1.visible===true) {
    playerselect11.visible = true;
    playerselect12.visible = true;
    playerselect13.visible = true;
  } else {
    playerselect11.visible = false;
    playerselect12.visible = false;
    playerselect13.visible = false;
  }
  if (player2.visible===true) {
    playerselect21.visible = true;
    playerselect22.visible = true;
    playerselect23.visible = true;
  } else {
    playerselect21.visible = false;
    playerselect22.visible = false;
    playerselect23.visible = false;
  }
  if (player1.visible===true) {
    if (mousePressedOver(playerselect11)) {
      nini.setAnimation("elk");
    }
    if (mousePressedOver(playerselect12)) {
      nini.setAnimation("cow_1");
    }
    if (mousePressedOver(playerselect13)) {
      nini.setAnimation("elephant_happy_1");
    }
    drawSprites();
  }
  if (player1.visible===false && (player2.visible===true)) {
    if (mousePressedOver(playerselect21)) {
      elk.setAnimation("elk");
    }
    if (mousePressedOver(playerselect22)) {
      elk.setAnimation("cow_1");
    }
    if (mousePressedOver(playerselect23)) {
      elk.setAnimation("elephant_happy_1");
  }
    drawSprites();
  }
  if (mouseDown("leftButton") && player2.visible === true && player1.visible === false) {
  player2.visible = false;
  elk.visible = true;
  nini.visible = true;
  sun.visible = true;
  ground3.visible = true;
  ground2.visible = true;
  ground.visible = true;
  start1.visible = true;
  start2.visible = true;
  elk.x = start2.x;
  elk.y = start2.y-5;
  nini.x = start1.x;
  nini.y = start1.y-5;
  }
  if ((mouseDown("leftButton"))&&(player1.visible===true)&&(player2.visible===false)) {
  player1.visible = false;
  player2.visible = true;
  }
  if (keyDown ("space")) {
    start.visible = false;
    player1.visible = true;
    player2.visible = false;
  elk.visible = false;
  nini.visible = false;
  sun.visible = false;
  ground3.visible = false;
  ground2.visible = false;
  ground.visible = false;
  start1.visible = false;
  start2.visible = false;
  elk.x = start2.x;
  elk.y = start2.y-5;
  nini.x = start1.x;
  nini.y = start1.y-5;
  }
  drawSprites();
```

### Freitag, der 23.11.2018<a name="27"></a>
Heute haben wir die letzen kleinen Änderungen wie Größen- und Geschwindigkeitsanpassungen am Projekt vorgenommen und sowohl die Projektseite als auch das Arbeitsprotokoll fertiggestellt.
