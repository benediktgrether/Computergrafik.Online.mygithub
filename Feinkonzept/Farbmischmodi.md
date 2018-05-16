Benedikt Grether </br>
MIB 4 HFU </br>
SOSE 18 </br>

# Grobkonzept - Farbmischmodi

## Kurze Zusammenfassung 
[ ] - Draft

***

## Definition Farbmischmodi

Farbmischmodi beziehen sich auf Ebenen eines Bildes.
Ebenen sind in der Regel undurchsichtig, das bedeutet die Oberste Ebene bedeckt die darunterliegenden Ebenen / darunterliegende Ebene. 
Mit den Ebeneneinstellungen für Farbmischmodi verändern wir das Verhalten solcher Ebenen.
Dabei werden Farbmerkmale einer Ebene mit den Farben der darunterliegenden Ebene verrechnet.
Zusätzlich ist es uns möglich mit den Mischmodi und einer direkten Verknüpfung auf einer Ebene bestimmte Farben oder Farbton auf der Verknüpften Ebene zu verändern.

Die Mischmodi bestimmen dabei, wie sich ein Mal - bzw. Bearbeitungswerkzeug auf die Pixel im Bild auswirken. Die Wirkung eines Mischmodus lässt sich wie folgt veranschaulichen.

- Die Ausgangsfarbe ist die Orginalfarbe im Bild.
- Die Mischfarbe ist die Farbe, die mit dem Mal- bzw. Bearbeitungswerkzeug aufgetragen wird.
- Die Ergebnisfarbe ist die beim Mischen der beiden Farben entstehenden Farbe.

*Bsp raussuchen*

> ## Definition Farbmischmodi
> *Page ist interaktiv*
>
>  

***

## Unterschiede zwischen den Farbmischmodi

Es gibt unterschiedliche Mischmodi, die teilweise ähnliche Funktionen haben.
Multiplizieren / Negativ Multiplizieren,
Weiches Licht / Hartes Licht.

- Multiplizieren
    - Multipliziert anhand der Farbinformationen in den einzelnen Kanälen die Ausgangsfarbe mit der Mischfarbe. Die Ergebnisfarbe ist immer eine dunklere Farbe.
    Beim Multiplizieren mit Schwarz entsteht die Farbe Schwarz
    Beim Multiplizieren mit Weiß bleibt die Farbe unverändert.

- Negativ Multiplizieren 
    - Multipliziert anhand der Farbinformationen in den einzelnen Kanälen die "Negative" oder Misch - Ausgangsfarbe. Die Ergebnisfarbe ist immer eine hellere Farbe. Bei "Negativ multiplizieren" mit Schwarz bleibt die Farbe unverändert. Bei "Negativ multiplizieren" mit Weiß entsteht Weiß. 
    Die Wirkung gleicht dem Übereinanderprojizieren mehrerer Dias.

- Weiches Licht
    - Je nach Mischfarbe werden die Farbe aufgehellt oder verdunkelt. Die Wirkung entspricht dem Anstrahlen des Bildes mit diffusem Scheinwerferlicht. Wenn die Mischfarbe (Lichtquelle) heller als 50%iges Grau ist, wird das Bild heller (ähnlich dem Abwedeleffekt). Wenn die Mischfarbe dunkler als 50%iges Grau ist, wird das Bild dunkler (ähnlich dem Nachbelichten). Durch Mischen mit reinem Schwarz oder Weiß wird ein deutlich dunklerer oder hellerer Bereich erzeugt, das Ergebnis ist jedoch kein reines Schwarz oder Weiß.

- Hartes Licht
    - Führt eine Multiplikation bzw. eine Negativmultiplikation der Farben durch (abhängigkeiten von der Mischfarbe). Die Wirkung gleicht dem Beleuchten des Bildes mit einem Spot-Strahler mit direktem Licht. Wenn die Mischfarbe(Lichtquelle) heller als 50%iges Grau ist, wird das Bild heller(ähnlich wie "Negativ Multiplizieren"). Diese Option eignet sich daher zum Hinzufügen von Lichtern zu Bildern. Wenn die Mischfarbe dunkler als 50%iges Grau ist, wird das Bild dunkler (ähnlich dem Multiplizieren). Diese Option eignet sich daher zum Hinzufügen von Tiefen zu Bildern. Das Malen mit reinem Schwarz, bzw Weiß erzeugt reines Schwarz, bzw Weiß.

> ## Unterschiede zwischen den Farbmischmodi
> *Page ist interaktiv*
>
> Auf ein Bild verschiedenen Farbmischmodi anwenden.
>   

***

## Histogramm

Ein Histogramm ist eine grafische Darstellung einer Häufigkeitsverteilung in Bezug auf ein quantitatives Merkmal.
<!-- Bei unserem Histogramm ist das quantitative Merkmal die Helligkeitsinformationen eines Farbpixels, sowie seiner Farbkanäle und die Tonwerte des Bildes. -->

In der Bildbearbeitung ist das quantitative Merkmal die Verteilung verschiedenen Helligkeitsstufen (Häufigkeitsverteilung) eines Bildes.
Das Histogramm zeigt dabei die Details in den Tiefen (linker Teil des Histogramms), in den Mitteltönen (Mitte) und in den Lichtern (rechter Teil). 

<!-- Ein Histogramm stellt die Verteilung eines Bildes auf die verschiedenen Helligkeitsstufen grafisch dar. Das Histogramm zeigt Details in den Tiefen (linker Teil des Histogramms), in den Mitteltönen (Mitte) und in den Lichtern (rechter Teil).  -->
<!-- Anhand eines Histogramms lässt sich erkennen, ob die Detailgenauigkeit im Bild ausreicht, um vernünftige Korrekturen vornehmen zu können. -->

Ein Histogramm bietet auch einen schnellen Überblick über den Tonwertbereich des Bildes, den sogenannten Key-Typ. Bei einem Bild mit niedrigen Farbwerten (Low-Key) konzentrieren sich die Details in den Tiefen, während die Details bei einem Bild mit hohen Farbwerten (High-Key) eher in den Lichtern anzutreffen sind. Bei einem Bild mit durchschnittlichen Farbwerten sind Details vor allem in den Mitteltönen sichtbar.


Durch den Einsatz von Farbmischmodi verändert sich dann diese Informationen, so das wir am ende ein neues Histogramm mit neuen Informationen bekommen, die wir versuchen zu Interpretieren.

> ## Unterschiede zwischen den Farbmischmodi
> *Page ist interaktiv*
>
> Aufbau eines Grundhistogramm mit einfacher Darstellung
>
> Auf der Seite soll ein Orginalhistogramm angezeigt werden, und ein Histogramm das sich verändert wenn man mit den Farbmischmodi spielt.
>   

***

## Verknüpfung mehrerer Mischmodi auf einem Bild

Auf ein Bild kann nicht nur ein Farbmischmodi angewendet werden, sondern viele Unterschiedliche.
Dabei verändert sich das Aussehen des Bildes und es können spezielle Effekte erziehlt werden.

> ## Unterschiede zwischen den Farbmischmodi
> *Page ist interaktiv*
>
> Verschiedene Blend-Modes zur verfügungstellen und auch überlagern lassen
> 

***