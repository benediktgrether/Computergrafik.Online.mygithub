# 3-D Modelierung

## Lernziele mit Definitionen

### Primitive Formen 

> - Der Lernende soll verstehen was Primitive Formen sind, und Beispiele nennen können wo diese Formen eingesetzt werden.


Primitive Formen in der 2D - Computergrafik
- Punkte
- Strecken
- Polygone 
- Kreise 
- Ellipsen 

Primitive Formen in der 3D - Computergrafik
- Kugel
- Würfel 
- Zylinder 
- Pyramiden
- Tube, Torus, Cone 
    - Übersetzen.

Oft werden diese Grundformen benützt um mittels Extrudieren und durch Verbinden über einen booleschen Modifier (Kapitel Modifier) schnelle einfache Formen zu krieren bis hin zu Komplexen 3D-Formen.

Mit diesen Primitiven Formen wird in den meisten fällen ein 3D Projekt gestartet.

<!-- Quellen 
    http://www.peachpit.com/articles/article.aspx?p=30594&seqNum=5
    http://findnerd.com/list/view/Different-Techniques-Used-for-3D-Modeling/11819/
 -->
<hr>

### Polygone

> - Der Lernende soll verstehen was Polygone sind. Denn Unterschied kennen und wiedergeben was High Poly und Low Poly ist.

Polygon sind benachbarte Punkte, die mit Linien verbunden und bilden die Kanten des Polygons.
Im zweidimensionalen, kartesischen Koordinaten System werden die Eckpunkte der Polygone durch die Zweikoordinaten in x - y - Achse und der Verbindungslinie definiert. Im dreidimensionalen Raum zusätzlich noch durch die z-Wert.

Ein Polygon bildet immer eine geschlossene Fläche, die in einer Ebene liegt. Bei gekrümmten Körpern wird die Fläche durch mehrere kleine Polygone angenähert oder durch gebogene Polygone gebildet.

Das Polygone mit den wenigstens Punkten und Kantenlinien ist das Dreieck. Werden mehrere Polygone miteinander verbunden, dann muss mindestens eine Kantenlinie zu zwei gleichen Polygonen gehören. Man spricht dann von Polygonnetzen.
  <!-- https://www.itwissen.info/Polygon-polygon.html
        https://www.autodesk.de/solutions/3d-modeling-software -->

Die häufigsten Polygonnetze sind dabei
- Dreiecksnetz
- Vierecksnetz

#### High und Low Poly Modelle 

Der Unterschied zwischen High und Low Poly Modellen ist ganz klar. 

- High Poly
    - Enthält mehr Polygone umd hochauflösende Resultate zu bekommen.

- Anwendungsbeispiele
    - Fotorealistische 3D Renderings (Bilder des Modells)
    - Detailausschnitte der Renderings, sogeannte "zoom-ins"
    - 3D Animation mit zoom-in Effekten

- Low Poly
    - Enthält weniger Polygone

- Anwendungsbeispiele
    - 3D Modelle die in Echtzeit bewegt werden müssen, wie z.B. in Produktkonfiguratoren
    - Augmented Reality
    - Virtual Reality
    - 3D Character und Umgebungen in 3D Spielen

<!-- http://www.virtualemotion.de/digitale-welt/item/16-was-ist-der-unterschied-zwischen-low-poly-und-high-poly-modellen -->

<hr>

### Edge - Flow 

> - Der Lernende soll die Edge-Flow Technik näher gebracht werden und er sollte danach sagen wofür die Edge - Flow Modellingtechnik verwendet wird im Bezug auch auf die Topologien (Polygone, Triangles, Quads).

#### Topologie 

Topologie bedeutet das Verhältnis zwischen Punkten, Kanten und Flächen. => welcher Eckpunkt mit welchem anderen eine Kante bildet und welche Kante mit einer anderen Kante dann eine Fläche bildet.
Es können grundsätzlich Flächen (Polygonen) aus beliebigen Eckpunkten und Kanten bestehen. Es ist aber zum Vorteil beim Modellieren nur Vierecke (Quads) zu verwenden.
<!-- https://sftp.hs-furtwangen.de/~mch/computergrafik/script/chapter03/lecture01/ -->

#### Edge - Flow 

Beim Edge - Flow werden Formen nachgebaut. Dies sind oft Organische Modelle wie Gesicherter.
Dabei wird eine Hintergrundbild zum Einsatz.

Beim Edge - Flow fängt man damit an das Modell in einzelne Bereiche zu Untergliedern, dabei hängt diese Unterteilungen an unterschiedlichen Faktoren zusammen.
- Optischer Fluss der Struktur
- Gewünschte Polygonanzahl
- Animationseigeneschaften des Modells

Danach fängt man an einzelnen Bänder anzulegen, um die einzelnen definierten Geometrien nachzubauen.
Danach Verbindet man die noch offenen Stellen mit den Verbundenen Bändern.

<!-- https://sftp.hs-furtwangen.de/~mch/computergrafik/script/chapter03/lecture01/ -->

<hr>

### Subdivision Surface Modelling

> - Der Lernende das Wissen weitergeben für die Benutzüng von Subdivision Modelling und Surface Modelling

Subdivison Surface sind durch den Computer errechneten, vereinfachte Annäherung an ein grobes Mesh.
Sie erlauben eine weiche Oberfläche von Objekten, ohne das eine Menge an Vertices und Faces erstellt werden müssen.
Objekte mit Subdivison Surfaces besitzen ein organisches Aussehen.

Trotzdem kann man bei der Benutzung des Subdivison Surfaces nachträglich wieder harte Kanten erstellt werden.
(Kapitel Modifier).

<hr>

### Clay Modelling und Sculpting

> - Der Lernende soll das Glay-Modellings und Sculpting erklären können.

Die Idee hinter dem Clay-Modelling ist es einfache oder auch komplizierte 3D Formen mit Hilfe dieser Technik zu Bewerkstelligen.
Clay heißt nämlich übersetzt *Knete*, und so geht man auch vor. Man überlegt sich seine Form wie sie später aussehen könnte und beginnt auf dieser Überlegungen z.b einen würfel zu Extrudieren und ihn in die entsprechende Form zu ziehen - Wie früher mit Knete.
Dabei ist das Extrudieren in jede richtung zulässig.

Wenn nun in dieses Knet-Model nun jetzt noch Strukturen eingearbeitet werden, geschieht das nun über die Sculpting Methode mit den Entsprechenden Werkzeugen.

<hr>


## Modifier und Operationen

Je nach Programm heißen die Funktionen die hier beschrieben werden anders.


### Defintion von Modifier und Operationen

> - Der Lernende soll verstehen und sagen können welche Vorteile es hat Modifier / Operationen zu benützen.

Modifier / Operationen sind Funktionen die in Unterschiedlicher Reihenfolge auf Objekte anwenden können.
Der Vorteil von Modifieren besteht auf ihre Arbeitsweisen - den Sie arbeiten Interaktiv, nicht destruktiv ( Solang man ihn nicht anwendet kann man ihn immer noch verändern ) und in belieber Reihenfolge.

Trotzdem hat die Reihenfolge in einem Modifikationsstabel einfluss auf das Aussehen des 3D Objektes.

<!-- https://de.wikibooks.org/wiki/Blender_Dokumentation:_Modifiers -->

<hr>

### Mirror

> - - Der Lernende soll den Vorteil des Mirror Modifiers wiedergeben können.

Für Spiegelsymmetrische Objekte ist es in der Regel zum Vorteil eine Seite zu modellieren und die andere Seite durch den Spiegel Modifier zu generieren.
Dabei benützt man den Mirror Modifier / Operation.
Dieser Modifier kann man dabei in x - y - z richtung Anwenden.
Bei der Anwendung des Mirrors Modifier muss man bestimmte Sachen beachten.
- Noch ergänzen.

<!-- https://de.wikibooks.org/wiki/Blender_Dokumentation:_Spiegelsymmetrische_Objekte -->

<hr>

### Boolescher Modifier / Operationen

> - Der Lernende soll die Unterschiede der verschiedenen Boolescher Operation erklären können.

Boolsche Operationen helfen dann weiter, wenn das Mesh zu umständlich zu Modellieren ist, aber sich leicht aus ader Kombination einfacher Grundformen zusammensetzen lässt.
Die Operationen wirken sich immer aus auf zwei geschlossene Objekte.

Die drei Einstellungen
- Intersect: Bildet die Schnittmenge zweier Objekte
- Union: Bildet die Vereinigung zweier Objekte 
- Difference: Ein Objekt wird vom anderen Objekt abgezogen

<!-- https://de.wikibooks.org/wiki/Blender_Dokumentation:_Boolsche_Operationen -->

<hr>

## Subdivison Surface - Catmull-Clark-Algorithmus

> - Der Lernende soll den Subdivision Surface Modifier kennen lernen und den Bezug zu dem Catmull-Clark-Algorithmus verstehen


[Seite 56 Catmull - Clark - Algo Berechnung](http://graphics.stanford.edu/courses/cs468-10-fall/LectureSlides/10_Subdivision.pdf)
- [ ] Craft - nachschauen wegen dem Catmull-Clark-Algo. 

<!-- https://de.wikibooks.org/wiki/Blender_Dokumentation:_Subdivision_Surfaces -->