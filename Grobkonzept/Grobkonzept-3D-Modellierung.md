Benedikt Grether </br>
MIB 4 HFU </br>
SOSE 18 </br>

# Grobkonzept - 3D Modellierung

## Kurze Zusammenfassung 
[ ] - Draft

***

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
> - Die Objekte können übereinander gestappelt werden - Vl eine kleine Szenerie nachbauen ? 
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

> ## Subdivision Surface
> *Page ist Interaktiv* 
>
> Würfel nehmen -> Subdivision Surface drüber legen und Abstufungen durchführen lassen
> Andere Modifiere ? 

***

Subdivison Surface 
http://www.holmes3d.net/graphics/subdivision/

***

# Clay Modelling und Sculpting