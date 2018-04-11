# Farbmischmodi | Mix - Blend - Mode

## Allgemein 

> ### Quelle: Wikipedia https://en.wikipedia.org/wiki/Blend_modes
>
> Blend modes (or Mixing modes[1]) in digital image editing and computer graphics are used to determine how two layers are blended into each other.
> The default blend mode in most applications is simply to hide the lower layer with whatever is present in the top layer

> ### Quelle: Simplefilter http://www.simplefilter.de/grundlagen/mischmodi.html
>
>Die Mischmodi gestatten die Verknüpfung der Tonwerte zweier Ebenen oder Farben und erlauben zahlreiche Effekte.
>Andere Namen für diese in allen Bildbearbeitungsprogrammen vorhandenen Modi sind Füllmethoden, Montageverfahren, Malmodi, Ebenenmodi, Zusammenfügen-Modi, Anpassungsmodi, Überblendmodi und Einkopiermodi.

> ### Quelle: Adobe https://helpx.adobe.com/de/photoshop/using/blending-modes.html
>
> Der in der Optionsleiste festgelegte Mischmodus bestimmt, wie sich ein Mal- bzw. Bearbeitungswerkzeug auf die Pixel im Bild auswirkt. Die Wirkung eines Mischmodus lässt sich wie folgt veranschaulichen:
> - Die *Ausgangsfarbe* ist die Originalfarbe im Bild.
> - Die *Mischfarbe* ist die Farbe, die mit dem Mal- bzw. Bearbeitungswerkzeug aufgetragen wird.
> - Die *Ergebnisfarbe* ist die beim Mischen der beiden Farben entstehende Farbe.

## Berechnung der Farbmischmodi | Mix-Blend-Mode

> ### Quelle : W3C https://www.w3.org/TR/compositing/#blendingnormal
>
>> Falls keine andere Quelle angegeben ist, wird immer auf das W3C verwissen
>
>Blending is the aspect of compositing that calculates the mixing of colors where the source element and backdrop overlap.
>Conceptually, the colors in the source element are blended in place with the backdrop. After blending, the modified source element is composited with the backdrop. In practice, this is usually all performed in one step. 
>The blending calculations must not use pre-multiplied color values.

#### Bezeichnung
- Cm: the result color after blending
- Cr: the result color
- B: the formula that does the blending
- Cs: the source color 
- Cb: the backdrop color
- $\alpha$b: the backdrop alpha

### Normal blend mode
>This is the default attribute which specifies no blending. The blending formula simply selects the source color.

$B(Cb,Cs) = Cs$

### Multiply blend mode
> The source color is multiplied by the destination color and replaces the destination.
>
>The resultant color is always at least as dark as either the source or destination color. Multiplying any color with black results in black. Multiplying any color with white preserves the original color. 
 
$B(Cb,Cs) = Cb*Cs$

![equation](http://latex.codecogs.com/gif.latex?B%28Cb%2C%20Cs%29%20%3D%20Cb*Cs)

### Screen blend mode
>Multiplies the complements of the backdrop and source color values, then complements the result.
>
>The result color is always at least as light as either of the two constituent colors. Screening any color with white produces white; screening with black leaves the original color unchanged. The effect is similar to projecting multiple photographic slides simultaneously onto a single screen.

$B(Cb, Cs)=1-((1-Cb)*(1-Cs))$<br>
$=Cb + Cs - (Cb*Cs)$<br>

- Nachrechnen ob sich das Teilweise wegkürzt.

### Overlay blend mode 
> ### Quelle Wikipedia https://en.wikipedia.org/wiki/Blend_modes#Overlay
>
>Overlay combines Multiply and Screen blend modes.[3] The parts of the top layer where the base layer is light become lighter, the parts where the base layer is dark become darker. Areas where the top layer are mid grey are unaffected. An overlay with the same picture looks like an S-curve.
>
>$f(a,b) = 2ab$ 
><br>if a < 0.5 otherwise<br>
>$f(a,b) = 1-2(1-a)(1-b)$


> ### Quelle W3C : https://www.w3.org/TR/compositing/#valdef-blend-mode-overlay
>
>Multiplies or screens the colors, depending on the backdrop color value.
>
>Source colors overlay the backdrop while preserving its highlights and shadows. The backdrop color is not replaced but is mixed with the source color to reflect the lightness or darkness of the backdrop.
>
>Overlay is the inverse of the hard-light blend mode. See the definition of hard-light for the formula.

$B(Cb, Cs) = HardLight(Cs, Cb)$
- Inverse Bilden.

if $(Cs <= 0.5)$

$B(Cb, Cs) =$ Multiply $(Cb, 2*Cs)$

Multiply

$B(Cb, Cs) = Cb * 2*Cs$

else

$B(Cb,Cs) =$ Screen $(CB, 2*Cs-1)$

Screen

$B(Cb, Cs)=2*(1-((1-Cb)*(1-Cs)))-1$


- Nachrechnen und die Inverse davon Bilden.

### Hard-Light blend mode
>Multiplies or screens the colors, depending on the source color value. The effect is similar to shining a harsh spotlight on the backdrop.

if $(Cs <= 0.5)$

$B(Cb, Cs) =$ Multiply $(Cb, 2*Cs)$

Multiply

$B(Cb, Cs) = Cb * 2*Cs$

else

$B(Cb,Cs) =$ Screen $(CB, 2*Cs-1)$

Screen

$B(Cb, Cs)=2*(1-((1-Cb)*(1-Cs)))-1$
<br>
<br>

### Soft-Light blend mode
>Darkens or lightens the colors, depending on the source color value. The effect is similar to shining a diffused spotlight on the backdrop.

if$(Cs <= 0.5)$

$B(Cb, Cs) Cb - ( 1-2*Cs) * Cb * (1-Cb)$

else

$B(Cb, Cs) = Cb +(2*Cs-1)*(D(Cb)-Cb)$

with

if$(Cb <= 0.25)$

$D(Cb) = ((16* Cb - 12)* Cb + 4) * Cb$

else 

$D(Cb)=\sqrt(Cb)$

### Photoshop Formel
> ### Quelle Wikipedia: https://en.wikipedia.org/wiki/Blend_modes#Soft_Light

$fphotoshop(a,b)= 2ab+a^2(1-2b)$ &nbsp;&nbsp; if $b<0.5$ otherwise <br>
$2ab(1-b)+\sqrt a(2b-1)$

### Darken blend mode
>Selects the darker of the backdrop and source colors.
>
>The backdrop is replaced with the source where the source is darker; otherwise, it is left unchanged.

$B(Cb,Cs)=min(Cb,Cs)$

### Lighten blend mode 
>Selects the lighter of the backdrop and source colors.
>
>The backdrop is replaced with the source where the source is lighter; otherwise, it is left unchanged.

$B(Cb,Cs)=max(Cb, Cs)$
>Note: The result must be rounded down if it exceeds the range.

### Color-Dodge blend mode
>Brightens the backdrop color to reflect the source color. Painting with black produces no changes.

if $(Cb == 0)$

$B(Cb, Cs) = 0$

else if $(Cs = 1)$

$B(Cb, CS)= 1$

else

$B(Cb,Cs) = min(1, Cb/ ( 1- CS))$

### Color-Burn blend mode
> Darkens the backdrop color to reflect the source color. Painting with white produces no change.

if$(Cb == 1)$

$B(Cb,Cs) = 1$

else if $()Cs == 0$

$B(Cb,Cs) = 0$

else 

$B(Cb, Cs) = 1- min(1, (1-Cb) / Cs)$

### Difference blend mode 
> Subtracts the darker of the two constituent colors from the lighter color.
>
>Painting with white inverts the backdrop color; painting with black produces no change.

$B(Cb, Cs) = | Cb - Cs|$

### Exclusion blend mode 
>Produces an effect similar to that of the Difference mode but lower in contrast. Painting with white inverts the backdrop color; painting with black produces no change

$B(Cb, Cs) = Cb + Cs - 2 * Cb * Cs$


[ ] Draft 

https://www.w3.org/TR/compositing/#blendingnonseparable

### Non-separable blend modes


