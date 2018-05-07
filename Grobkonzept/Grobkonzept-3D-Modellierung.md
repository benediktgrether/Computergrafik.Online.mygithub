Benedikt Grether </br>
MIB 4 HFU </br>
SOSE 18 </br>

# Grobkonzept - 3D Modellierung

## Kurze Zusammenfassung 
[ ] - Draft

***


# 1.) 3D Modellingstechnik

## Grundformen

Die Computergrafik setzt sich am Anfang in den meisten Fällen aus Grund Formen zusammen.

Im Bereich der 2D - Computergrafik besteht dies aus den Elementen

- Punkte
- Strecken 
- Polygone
- Quadrate  
- Kreise 
- Ellipsen

Die Grundformen in der 3D Computergrafik sind
- Kugel 
- Würfel 
- Zylinder 
- Pyramiden
- Röhre
- Kegel
- Torus 
    - Wulstartige geformte Fläche mit einem Loch in der Mitte
    - Können Rettungsringe oder Donuts sein.


### 2D Computergrafik

In der 2D Computergrafik kann man mittels Quadrate u.ä. schnelle Grafische Formen zusammenbauen, und diese durch löschen und zusammenfügen Logos und ähnliches Bauen.

### 3D Computergrafik

Oft werden diese Grundformen zum Beginn eines Projektes benützt - vorallem in der 3D Computergrafik.
Um das Objekt den Bedürfnisse anzupassen, könnte man diese dann durch Extrudieren in die gewünschten Formen bringen, oder mittels Modiefier / Operationen verändern. (Kapitel Modifier / Operationen ).
Es besteht auch die Möglichkeit bei diesen Grundformen, diese miteinander zu Verbinden und dadurch auch komplexe 3D Grafiken bauen.

> ## Screen Grundformen
> *Page ist interaktiv*
>
> Die 2D und 3D Objekte werden vorgestellt
> Kurzes Beispiel gezeigt für die 2D Computergrafik erstellung eines Objektes.
> Interaktion mit den 3D Objekten
> - Verschiedene 3D Objekte können ausgewählt werden.
> - Die Objekte können übereinander gestapelt werden - Vl eine kleine Szenerie nachbauen ? 
> 
> *Screens*
> Beschreibungstext der einzelne Elemente müssen dazu 
> 2-D und 3-D Objekte


***

## Polygone

Bei einem Polygon sind benachbarte Punkte mit Linien verbunden und bilden die Kanten des Polygons.
Im zweidimensionalen, kartesischen Koordinaten System werden die Eckpunkte der Polygone durch die Zweikoordinaten in x - y- Achsen und der Verbindungslinie definiert. Im dreidimensionalen Raum zusätzlich noch durch den z - wert.

Ein Polygon bildet immer eine geschlossene Fläche, die in einer Ebene liegt. Bei gekrümmten Körpern wird die Fläche durch mehrere kleine Polygonen angenähert oder durch gebogene Polygone gebildet.

[Link](# Screen Polygone)

Polygone mit den wenigstens Punkten und Kantelinien ist das Dreieck. 
Werden mehrere Polygone miteinander verbunden, dann muss mindestens eine Kantenlinie zu zwei gleichen Polygonen gehören. Man spricht dann von Polygonnetzen.

Die häufigsten Polygonnetze sind dabei
- Dreiecksnetz
- Vierecksnetz

[Link](# Screen Polygone)

### High und Low Poly Modelle

Der Unterschied zwischen High und Low Poly Modellen kann man ganz einfach über deren Namen weitergeben. 

| High Poly | Low Poly |
| ------------- | ------------- |
| Enthält mehr Polygone um hochauflösende Resultate zu bekommen  | Enthält weniger Polygone um schnelle Resultate zu erhalten  |

#### Anwendungsbeispiele

##### High Poly 
- Fotorealistische 3D Renderings (Bilder des Modells für Filme)
- Detailauschnitte der Renderings, sogenannte "zoom-ins"
- 3D Animationen mit zoom-in Effekt

##### Low Poly
- 3D Modelle die in Echtzeit bewegt werden müssen
    - Produktkonfiguratoren
- Augmented Reality / Virtual Reality
- 3D Character und Umgebung in 3D Spielen



> ## Screen Polygone
> *Page ist Interaktiv* 
>
>
> Polygon aufzeigen mit Eckpunkt -> das dann mit einer Linie verbunden wird, und dadraus dann ein Polygon Netz entsteht.
>
> Aufzeigen der Polygonnetze
> - Dreiecksnetz 
> - Vierecksnetz
>
> ### High und Low Poly Modelle
>
> - User kann Polygon Anzahl verringern und das Objekt zeigt es in echtzeit an wie Polygone im Polygonnetz hinzukommen oder entfernt werden.
> 
> Allgemeines Aufzeigen von 3D Objekten - High and Low Poly

***

## Edge - Flow

### Topologie

Bei der Topologie dreht es sich um die Verhältnise zwischen Punkten, Kanten und Flächen. 
Das bedeutet, welcher Eckpunkt mit welchem anderen eine Kante bildet und welche Kante mit einer anderen Kante eine Fläche bildet. 
- siehe Polygone
Es können grundsätzlich Flächen (Polygonen) aus beliebigen Eckpunkten und Kanten bestehen. Es ist aber zum Vorteil beim Modellieren nur Vierecke (Quads) zu verwenden.

### Edge - Flow 

Beim Edge - Flow werden in der Regel Formen nachgebaut die Organischen Ursprung haben wie z.B Gesichter.
Um dabei eine bessere Detailtreue zu bekommen, wird hierbei (und bei vielen verschiedenen weiteren Modeltechniken) ein Hintergrundbild gelegt. Dabei möchte man soweit wie es möglich ist die Exakte Form nachmodellieren.
> Speziel für Organische Lebewesen wird noch weiter versucht die Orginalen Muskelpartien nachzubilden, falls später dieses Objekt animiert wird und diese Anatomisch richtig bewegt werden
Die Vorgehensweiße bei der Edge - Flow Modelling Technik besteht daraus , Bereiche zu Unterteilen.
Dabei hängt dies von verschiedenen Faktoren ab.
- Optischer Fluss der Struktur 
- Gewünschte Polygonanzahl
- Animationseigenschaften des Modells

Danach fängt man an einzelne Bänder anzulegen, um die einzelnen definierten Geometrien nachzubauen.
Danach verbindet man die noch offenen Stellen mit den Verbundenen Bändern.

> ## Screen Edge - Flow
> *Page ist nicht Interaktiv* 
>
> Topologien aufzeigen und nochmal einen vergleich zu Polygonen ziehen
> Edge - Flow zeigen.
> - Elemente unterteilen
> - Bänder anlegen 
> - Verbinden
> - Endergebnis

***

## Subdivision Surface

Bedeutung 
- Subdivision Surface = Unterteilungsflächen
- Limes = Grenzwerte 

Bei der Verwendung des Subdivision Surface wird durch den Computer eine Berechnung in verschiedenen Stufen durchgeführt, die eine Annäherung an ein grobes Mesh erledigt. -> Limes (Grenzwert)
Mit dem Subdivision Surface soll das Objekt eine Runde/Organische Struktur bekommen, aber weiterhin auch die Möglichkeit bieten das die Struktur weiterhin auch noch harte Kanten besitzt.

<!-- Dabei liegt ein glattes Polygone Grundnetz zur Verfügung und wird durch mehrfache Abstufung in neue Teilbereiche eingeteilt. -->

Dabei gibt es zwei Vereinfachungsschematas die in Kategorieren eingeordnet werden.

- Approximierende 
    - Die Limesflächen kann innerhalb oder außerhalb des Ausgangsgitters zu liegen kommen. 
    - Bei jedem Rekursionsschritt liegen die neu Erzeugten Punkte nie auf den Limesflächen.

- Interpolierende
    - Werden benützt wenn die Limesfläche die Punkte des Ausgangsgitter interpolieren soll.
    - Die Punkte des Ausgangsgitters und die durch jeden Rekursionschritt neu erzeugten Punkte immer auf den Limesflächen liegen.

| Approximierende | Interpolierende |
| ------------- | ------------- |
| Catmull-Clark  | Butterfly  |
| Doo–Sabin     |  Kobbelt |
| Loop  |       |
| Mid-Edge  |       |
| v3        |       |

Ein weiteres Unterscheidungskriterium, ist die Kategorisierung in Schemata, die nur auf Gittern aus Polygone mit bestimmter Punktanzahl bestehend. Einige solcher Schemata benötigen beispielweise ein Ausgangsgitter, das nur aus Dreiecken oder Vierecken besteht.


<!-- Subdivison Surface 
http://www.holmes3d.net/graphics/subdivision/ -->

> ## Subdivision Surface
> *Page ist Interaktiv* 
>
> Würfel nehmen
>
> Subdivision Surface drüber legen und Abstufungen durchführen lassen
>
> Andere Modifiere ? 
>
> Harte Kanten weiterhin erzeugen.
>
> Umsetzung ? 

***


## Clay Modelling und Sculpting


### Clay Modelling

Die Idee hinter Clay-Modelling ist es komplizierte 3D-Formen oder organisch aussehende Objekte wie Pflanzen, Tiere , Aliens mit dieser Technik herzustellen.
Clay bedeutet übersetzt *Knete*.
Man nimmt also eine Grundform, z.B einen Würfel und fängt an seine Flächen zu Unterteilen und die Unterteilten Flächen zu Extrudieren. Dabei werden oft die Extrudierten Flächen immer weiter Unterteilt, bis zum gewünschten Ergebnis.

## Sculpting

Beim Sculpting nimmt man jetzt z.B das Clay-Modelling und arbeitet mit dem Sculpting Werkzeug nun gewünschte Strukturen rein.

- Falten 
- Narben  usw.

> ## Clay Modelling und Sculpting
> *Page ist nicht Interaktiv* 
>
> ### Clay Modelling
> Würfel nehmen
>
> Flächen Unterteilen
>
> Extrudieren
>
> weitere Flächen Unterteilen
>
> Gewünschtes Ergebniss da ist.
>
> ## Sculpting
>
> Auf Basis des Clay Modelling Strukturen einarbeiten.


***

# 2.) Modifier und Operationen

Je nach Programm heißen die Funktionen die hier beschrieben teilweise anders.

## Defintion von Modifier und Operationen

Modifier / Operationen sind Funktionen die in Unterschiedlicher Rheinfolge auf das zu Modullierende Objekt angewendet werden können. - Die Reihenfolge auf einem Modifikationsstabel hat trotzdem einen Einfluss auf das Aussehen des 3D Objektes.

Der Vorteil von Modifieren besteht auf ihrer Arbeitsweise.
- Arbeiten Interaktiv
- nicht destruktiv

=> Solange man die Modifier / Operationen nicht anwendet kann man diese immer noch verändern.

> ## Defintion von Modifier und Operationen
> *Page ist Interaktiv* 
>
> Modifier zeigen und den Modifierstabel verändern lassen.
>

***

## Mirror - Modifier / Operation

Für Spiegelsymmetrische Objekte ist es zum Vorteil, nur eine Seite des 3D Objektes zu realisieren.
Danach benützt man den Mirror - Modifier / Operation um es auf die andere Seite zu spiegeln.
Der Mirror Modifier / Operation kann dabei grundsätzlich auf die x-y-z - Achse angewendet werden. 

Desweiteren hat der Mirror Modifiere / Operation noch weiter Einstellungsmöglichkeiten. 
- Objekt zusammengefügt werden soll.

- Only Blender?
    - Clipping
    - Vertex Group 

Falls die Spiegelseite noch unterschiedlichere Elemente hat die bearbeitet werden müssen, könnte man hierfür dann den Modifier anwenden.

> ## Mirror - Modifier / Operation
> *Page ist Interaktiv* 
>
> Objekt in x-y-z richtung Spiegeln lassen.
>
> Objekt Mergen , Clipping und aufzeigen der Vertex Group

***

## Booleasch Modifier / Operation

Die Boolschean Modifier / Operationen helfen dann weiter, wenn das Mesh zu umständlich zu Modellieren ist, aber sich leicht aus der Kombination einfacher Grundformen zusammensetzen lässt.
Die Operationen wirken sich dabei immer auf zwei geschlossene Objekte aus.

Bei dem Boolschean Modifier / Operation gibt es drei Einstellungen.

- Intersect: Bildet die Schnittmenge zweier Objekte.
- Union: Bildet die Vereinigung zweier Objekte.
- Difference: Ein Objekt wird vom anderen Objekt abgezogen.

> ## Mirror - Modifier / Operation
> *Page ist Interaktiv* 
>
> Die 3 Booleaschen Modifier durchführen lassen und verschiedenen Schnittmengen Bilden lassen
>

***

## Subdivision Surface - Catmull-Clark-Algorithmus

Siehe oben.

- Berechnung des Catmull-Clark-Algorithmus

Wenn ich noch was dazu finde, die anderen Schemata noch ausarbeiten.

> ## Subdivision Surface - Catmull-Clark-Algorithmus
> *Page ist Interaktiv* 
>
> Berechnung auflisten und anhand eines Objektes, die verschiedene Schematas ausführbar machen.
>

***