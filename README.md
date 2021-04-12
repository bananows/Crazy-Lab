# Crazy-Lab
Projekt von Samed und Bjarne

Informatik 12bc

Das Projekt ist im Ordner "files" zu finden und runterzuladen.

<h2>Vorwort</h2> 
Auf dieser Seite präsentieren wir unser Spiel und bieten Einblicke in die Mechaniken unseres Codes. Wir hatten trotz der Coronasituation und den Schwierigkeiten des Homeschoolings Spaß am Programmieren unseres Spiels.


<h2>Inhaltsverzeichnis</h2>

* <a href="#spielprinzip">Spielprinzip</a>
* <a href="#greenfoot">Greenfoot!</a>
* <a href="#programmierung">Programmierung</a>
    + <a href="#myworld">MyWorld</a>
    + <a href="#actor">Actor</a>   
    + <a href="#turtle">Turtle</a>
    + <a href="#wall">Wall</a>
    + <a href="#rocket">Rocket</a>


<h2>Programmierung</h2>

<h2 id="spielprinzip">Spielprinzip</h2>

Unser Spiel ist ein Labyrinthspiel, dessen Hauptcharakter eine Schildkröte ist, die sich im Labyrinth verlaufen hat. Ihr Ziel ist es, zur Rakete zu gelangen und mit dieser aus dem Labyrinth zu fliehen. Das Besondere und die Schwierigkeit an unserem Spiel ist es, dass man die Schildkröte nicht beliebig selbst nach vorne bewegen kann und bei einer Kollision mit der Wand wird der Spieler wieder ganz zum Anfang teleportiert. Die Schildkröte ist mit den Pfeiltasten zu steuern. Der Spieler muss sich auf die verschiedenen Wege konzentrieren und dabei achten, dass er nicht in eine Sackgasse läuft. Nachdem der Spieler die Rakete erreicht hat, erwartet ihn jedoch ein düsteres Geheimnis.


<h2 id="greenfoot">Greenfoot</h2>

Greenfoot ist eine Programmiersprache, welche auf Java beruht. Sie wird hauptsächlich zu Ausbildungs- und Lehrzwecken benutzt, dies erfolgt meistens in Schulen und Universitäten. Da Greenfoot jedoch auf Java beruht, ist es auch möglich eher komplexere Programmierungen zu kreieren. Greenfoot wurde mit der Unterstützung von Oracle an dem King´s College London entwickelt. Als Hauptentwickler zählt Michael Kölling. Die erste Version von Greenfoot wurde 2006 veröffentlicht. Greenfoot bietet im Programm selbst viele Tutorialvideos und Erklärungen an. Das Besondere ist ein Klassendiagramm , welches dem Programmierer die Übersicht vereinfachen soll und somit die verschiedenen Klassen visualisieren. Dies hilft gerade Programmierneulingen die objektbasierte Programmiersprache Java zu lernen, da sie im Gegensatz zum reinen Code in anderen Programmierumgebungen durch Struktur und Visualisierung Abhilfe schafft. Die Erklärungen sind in Englisch und in Deutsch verfügbar.


<h2 id="programmierung">Programmierung</h2>

<h2 id="myworld">MyWorld</h2>

Die MyWorldklasse dient zur Definition der allgemeinen Gegebenheiten in unserem Programm. Ein Teil der MyWorldklasse ist ein Bereich mit dem Titel „public MyWorld“, welcher für alle Actor öffentlich Informationen zu den allgemeinen Variablen bereitstellt, auf welche jeder Actor zugreifen kann. In ihm sind bei uns die Variablen „wall“, „rocket“ und „turtle“ definiert und die Position, an welcher sie zu Beginn des Spiels platziert werden.
Unter dem Methodenteil, mit dem Befehl „private void prepare()“, sind all unsere Wände mit ihrer Länge und Breite definiert und platziert. Das Besondere ist, dass alle Wände in die Klasse des Actors „wall“ fallen und somit die gleichen Eigenschaften haben. Es wird lediglich eine Kopie erstellt, welche am entsprechenden Ort platziert wird. Zu Angabe der Position werden x- und y- Koordinaten benutzt, genau so wie zur Angabe von Breite und Länge. Die Besonderheit bei der Greenfootprogrammierung ist, dass die x-Achse als Spiegelachse für das Koordinatensystem dient. 

<h2 id="actor">Actor</h2>

Ein Actor ist ein Objekt , welches in der Greenfootwelt existiert. Jeder Actor hat eine bestimmte Position und ein individuelles Aussehen in der Welt. Verschiedene Objekte können als Unterklassen des Actors erschaffen und definiert werden. Im Editor der Actorklassen können mithilfe der „act“-Methode die Funktionen der jeweiligen Actor beim Start des Spiels bestimmt werden.

<h2 id="turtle">Turtle</h2>

Die Turtleklasse ist die erste Unterklasse der Actor und sie definiert unseren Hauptspielcharakter. In ihr steckt das Aussehen einer Schildkröte, ihre Größe und ihre Funktionen. Die Funktionen sind hierbei die Steuerung und das Ereignis bei einer Kollision mit der Wand. Die Schildkröte kann mit den Pfeiltasten in die jeweilige Richtung der Pfeile bewegt werden. Bei einer Kollision mit der Wand wird die Schildkröte wieder an den Start gesetzt. 
Die Bewegung nach vorne ist dauerhaft mit „move(1)“ bestimmt. 
Die Bewegung in die bestimmten Richtungen haben wir mit „if(Greenfoot.isKeyDown(„Taste“)) und „setRotation(„Gradzahl“) programmiert.
Das Ereignis im Falle einer Kollision haben wir mit „if(isTouching(name.class)) und „setLocation(x,y)“ definiert. 


<h2 id="wall">Wall</h2>

Die Wallklasse ist die zweite Unterklasse der Actor und sie definiert die Wände unseres Labyrinths. Durch Rechtsklick und das Klicken auf „new Wall“ kann eine neue Wand mit einer selbst bestimmbaren Breite und Länge kreiert werden. Dazu gibt man einfach die gewünschten x- und y- Werte ein.
Durch den Befehl „this.height“ und „this.width“ wird angegeben, dass Höhe und Breite bei jedem Objekt einzeln abgefragt werden müssen durch ein Dialogfenster. Die angegebenen Werte sind „neue Höhe und Breite“, welche später zur Skalierung des Bildes der Wand genutzt werden mit dem Befehl „getImage().scale(width, height)“. 

<h2 id="rocket">Rocket</h2>

Die Rocketklasse ist die dritte und letzte Unterklasse der Actor und sie definiert die Rakete und somit das Ziel unseres Spiels. Die Position der Rakete wird bereits in der MyWorld-Klasse definiert. In der Rocketklasse wird ausschließlich die Größe der Rakete und die Richtung, in welche sie zeigt, definiert.
Dazu haben wir erneut den „getImage().scale(x, y)“ und den „setRotation(Gradzahl)“ Befehl benutzt.

