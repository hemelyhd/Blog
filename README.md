# Blog
INFORMATIK
### 21.08. Dienstag
Nach einer Einführung von Herrn Buhl in die Thematik und der Vorstellung der Projektstruktur, haben wir uns ein eigenes Github Konto erstellt. Heute haben wir uns über die Programme Github, Greenfoot und the Beauty and Joy of Computing informiert und probiert sie so gut wie möglich zu verstehen. Deshalb haben wir heute größtenteils im Internet recherchiert und uns die gestellten Links, sowie weitere Tutorials angeschaut.

### 27.08. Montag
Durch viel Recherche zuhause konnten wir uns ein Bild von den Programmen machen (vor allem von Greenfoot) und haben uns dementsprechend auch entschieden, mit diesem zu arbeiten. Das heißt zwar, dass wir wahrscheinlich mehr Arbeit zuhause reinstecken müssen, weil uns schon aufgefallen ist, dass es wahrscheinlich besonders jetzt am Anfang schon schwieriger ist mit der Programmiersprache (mit der wir noch nie zuvor in Verbindung gekommen sind), als mit den Code-Bausteinen aus The Beauty and Joy of Computing zu arbeiten.

### 28.08. Dienstag
Nach weiterer Recherche und dem Erstellen einer Weltraumwelt, haben wir einen ersten Actor in diese gesetzt: Eine Sausage! An dieser haben wir unsere ersten Codes angewendet und ein bisschen herumprobiert. Dabei haben uns auch die ersten Schritte aus dem Informatikbuch, welches wir uns beide zum lernen ausgeliehen haben geholfen. Desweiteren haben wir eine Raktete in die Welt gesetzt und ihr erstmal eine konstante Bewegung gegeben, sodass sie immer von Weltrand zu Weltrand fliegt. Dafür haben wir die Codes if ... move() und turn() benutzt. Ein Problem, das besteht ist, das wir nicht wissen wie wir den Actor in der Welt behalten, bis jetzt mussten wir ihn immer neu mit in die Welt ziehen.

### 10.09. Montag
Wir haben eine Lösung für unser Problem gefunden! Es war nicht möglich einen Actor mit Rechtsklick und "Save the World" zu speichern, beziehungsweise war es das, man konnte es dann aber komischerweise nicht mehr ändern. Deshalb haben wir den Actor nun in der Programmierung der Welt mithilfe von prepare() verankert, sodass er sofort bei Entstehung der Welt an bestimmten Koordinaten erscheint. Langsam wird es einfacher das Programm und vor allem die Fehlermeldungen, die das Programm anzeigt, zu verstehen und eigenständig Lösungen zu finden. Wir haben außerdem nun eine Idee für unser Spiel: Es heisst "Es geht um die Wurst", und das tut es wortwörtlich, das Ziel ist es eine Wurst an ein Ziel zu bringen und dabei den Raketen auszuweichen.

### 11.09. Dienstag
Heute haben wir unser Spielkonzept ausgebaut und verfeinert. Dafür haben wir einen neuen Actor, eine kleine Pfanne auf der die Sausage anfangs liegt in die Welt gesetzt. Außerdem haben wir einen großen Teller am oberen Bildschirmrand hinzugefügt, auf dem die Sausage als Ziel landen muss. Hier war es allerdings zuerst eine Herausforderung herauszufinden, wie man die Größe des Actors anpasst, das haben wir dann aber doch hingekriegt.

### 17.09. Montag
Heute haben wir das Konzept unseres Spiels verändert, es ist nun ein Multiplayer-Spiel. Dafür haben wir noch eine weitere Bratpfanne und eine weitere Sausage hinzugefügt. Dementsprechend haben wir das Format der MyWorld geändert. Nun geht es darum, wer als erstes den Teller berührt.

### 18.09. Dienstag
Heute haben wir an unserem neuen Actor gearbeitet: Bullet. Bullet ist ein Schwein, welches durch den Weltraum schwebt. Bei einer Berührung von Bullet und einer Sausage, wird die Sausage schneller (das haben wir einfach mit if... move(schneller als Ausgangsgeschwindigkeit) programmiert). Dieser Boost kann im Spiel ein Vorteil sein, weil die Sausage des Spielers schneller zum Teller kommt, aber auch ein Nachteil, weil sie somit auch unkontrolliert gegen eine Rakete geboostet werden kann.

<img width="180" alt="schwein" src="https://user-images.githubusercontent.com/43174249/48730424-99f48f80-ec3a-11e8-8d4e-924b5d359f70.png">


### 22.10. Montag
Wir haben an der Programmierung der Raketen etwas verändert, es sind nicht mehr einzelne Actor, sondern gehören einer Actorklasse an, haben die gleichen Befehle, starten aber an unterschiedlichen Koordinaten. Des Weiteren haben wir noch mehr Raketen platziert, um die Schwierigkeit zu erhöhen.

<img width="606" alt="mehrere raketen bestimmter platz" src="https://user-images.githubusercontent.com/43174249/48730428-9c56e980-ec3a-11e8-8f59-3d30356b942e.png">

### 23.10. Dienstag
Heute haben wir probiert, ein wichtiges Problem zu lösen. Wir haben erst einmal unsere Programmierung umgeschrieben. Nach einem Gespräch mit Herrn Buhl wurden aus zwei Actorn (Sausage 1 und Sausage 2) nur noch ein Actor: Sausage. Dementsprechend haben wir ihnen trotzdem unterschiedliche Befehle (unterschiedliche Tasten zum Bedienen) gegeben.

<img width="546" alt="2 sausage untersch befehle" src="https://user-images.githubusercontent.com/43174249/48730257-15a20c80-ec3a-11e8-9ee4-df704693ab27.png">


### 29.10. Montag
Heute haben wir an der Expolosion gearbeitet, die entstehen soll, wenn die Rakete auf eine Sausage trifft. Zuerst wollten wir die Explosion mit dem Code set.Transparency() durchsichtig hinter der Sausage mitlaufen lassen, und sie erscheinen lassen, sobald sich Sausage und Rakete berühren. Dies hat allerdings nicht wirklich geklappt. Sie wird nun per Signal an myWorld von ihr aus in die Welt gesetzt. Das ist aber leider noch nicht ganz fehlerfrei, denn es entstehen viele Explosionen, solange Rakete und Sausage sich noch berühren, was zur Stocken des Spiels führt.

### 30.10. Dienstag
Heute haben wir die Lösung für das Explosionsproblem mithilfe dieses neuen Codes gefunden:

<img width="531" alt="explosion neu nur 1mal" src="https://user-images.githubusercontent.com/43174249/48729921-3158e300-ec39-11e8-83ed-84c9405c3d84.png">

Er stellt sicher, dass nur ein Explosionsbild entsteht und der Befehl "neues Bild produzieren" nicht durchgehend aufgerufen wird.
Wir haben uns außerdem verschiedene Feuerwerksbilder aus dem Internet angeschaut und ausgewählt, welches bei Gewinn einer Sausage erscheinen soll und wir groß es sein soll. mit IF touches usw haben wir das Bild von myWorld in die Welt gesetzt, von der Programmierung her haben wir uns an das gleiche Konzept wie bei der Explosion gehalten.

<img width="531" alt="wie bei expl neu confetti 1mal wenn s p --noch nicht top" src="https://user-images.githubusercontent.com/43174249/48729803-d626f080-ec38-11e8-90b9-70ed06b7d835.png">


### 06.11. Montag
Wir haben heute probiert, die Probleme aus der letzten Stunde zu lösen:

1. Wenn die Sausage den Teller berührt, wird ein Feuerwerk erzeugt, die kommt allerdings zu früh. Die Sausage berührt gerade einmal den unsichtbaren Rand des Tellerbilds, aber nicht den Teller auf dem Bild.
2. Wenn die Sausage eine Rakete berührt, wird eine Explosion erzeugt, diese soll aber nach circa 5 Sekunden wieder verschwinden. Zuerst haben wir den Code delay verwendet, dieser hat jedoch das komplette Spiel verzögert. Im Internet und teilweise auch im Buch sind wir auf geeignete Codes gestoßen, diese konnten wir jedoch nicht verwenden, weil wir eine andere Version von Greenfoot haben und sie sich so nicht überschreiben lassen. Ein Versionswechsel wäre also in Zukunft auch eine Lösung für viele Probleme.

### 12.11. Montag
Wie in den letzten Stunden, haben wir mit unserem Programm gekämpft, welches sobald eine Explosion entsteht, das Spiel haken lässt und mehrere Explosionen entstehen, wenn sich die Sausage weiterbewegt und erneuert auf eine Rakete trifft. In diesen Fällen wurden die Actor immer zu Greenfoot Füßen und das Programm stürzt ab. Heute haben wir das Problem mit folgendem Code gelöst, der dafür sorgt, dass nur ein Explosionsbild entsteht und das Spiel danach normal weiterläuft ohne zu haken. FOTO 

### 13.11. Dienstag Emely allein (??)
