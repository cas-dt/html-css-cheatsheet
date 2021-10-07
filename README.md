# HTML- und CSS-Basics

## Vorbemerkungen

Ziel dieses Textes ist nicht, dass du ihn nach einmal durchlesen verstehst. Er enthält mehr Information, als nötig. Wenn es dir zu kompliziert wird, kannst du Details überspringen.

Dieser Text soll dich beim Entdecken von HTML und CSS unterstützen. Aber beim Coding gilt «probieren geht über studieren». Wenn es keine Freude macht, bringt es nichts.

## Definitionen

HTML: ‘Hypertext Markup Language’

CSS: ‘Cascading Style Sheets’

- HTML- und CSS schreiben ist Coding.
- HTML- und CSS schreiben ist ernsthafte Programmierung. Wer etwas anderes behauptet, beweist nur seine Unkenntnis.

HTML dient zur Strukturierung von Dokumenten, so dass sie adäquat gerendert werden können. Und dass sie von interpretierender Software (Suchmaschinen, Text-to-Speech, Übersetzung etc.) gut evaluiert werden kann.

CSS dient dazu, HTML-Dokumente zu gestalten.

Ein Browser ist eine Software, die HTML-Dokumente rendert.

HTML ist eine *Auszeichnungssprache*. CSS ist eine *Stylesheet-Sprache*.

JavaScript (JS) ist eine Programmiersprache, mit der sich beeinflussen lässt, wie HTML-Dokumente im Browser gerendert werden. Sie kann auch dazu gebraucht werden, Inhalte zu laden, bewegte Bilder zu programmiern und Server-seitige Software zu schreiben. Wir werden JS nicht anschauen, weil uns die Zeit fehlt. Wenn es dich interessiert, beginne mit [Daniel Shiffmans Youtube-Kanal ‘The Coding Train’](https://www.youtube.com/c/TheCodingTrain).

## HTML-Syntax

- HTML besteht aus *Tags*
- *Tags* grenzen Elemente eines Dokumentes voneinander ab.
- *Tags* definieren, in welcher Beziehung Elemente eines Dokumentes zu einander stehen.
- *Tags* definieren Hierarchien im Dokument.
- Ein Tag wird durch eckige Klammern gekennzeichnet: `<>`
- In den eckigen Klammern steht der Name des Tags: `<body>`
- Der Name des *Tags* hat eine Bedeutung (*Semantik*).
- Die meisten Tags treten paarweise auf und fassen ein Text-Element ein: `<h1>Eine Überschrift</h1>`
- der *schliessende Tag* wird mit einem Schrägstrich `/` gekennzeichnet.
- In Tags kann zusätzlich zum Namen noch weitere Information enthalten sein, in der Regel als *Eigenschaft-Wert-Paar*: `href="https://info.cern.ch"`
- So ein Zusatz wird als `Attribut` bezeichnet: `<a href="https://info.cern.ch">`
- Beispiele für *Attribute* sind Link-Ziele, Klassen oder eine ID.

## CSS-Syntax

- CSS besteht aus Regeln.
- Eine *CSS-Regel* besteht einem oder mehrere *Selektoren* und einer *Deklaration*.
- Ein *Selektor* bezeichnet HTML-Elemente, indem er sie benennt:
  - bei ihrem *Namen* `h1`
  - bei ihrer *Klasse* `.irrelevant-information`
  - bei ihrer *ID*: `#self-destruct-button`
- Eine Deklaration wird von geschweiften Klammern eingefasst: `{ }`
- Die geschweiften Klammern enthalten *Eigenschaft-Wert-Paare*: `color: red;`
- Am Ende jedes Wertes steht ein Strickpunkt: `;`
- CSS kennt keine Leerzeichen. Ohne Strichpunkte «verklebt» alles.
- Stylesheets können auch Dinge enthalten, die sich nicht an diese Konventionen halten. Solche Ausnahmen beginnen mit einem `@` und werden darum als *@-Regeln* bezeichnet. Z.B. *Media-Queries* und *Keyframes* für Animationen.

Ein Stylesheet kann direkt in ein HTML-Dokument geschrieben werden, einzelne Deklarationen sogar direkt in einzelne Tags. Ich möchte dies nicht empfehlen.

## Typische HTML-Tags

`html` das Dokument

`head` Informationen zum Dokument, wird nicht gerendert

`body` Der Inhalt – das, was gerendert wird

`h1` Überschrift erster Ordnung (übergeordnet)

`h6` letzte untergeordnete Überschrift

`p` Paragraph

`ul` ungeordnete Liste

`ol` Aufzählung

`li` Listen-Element (‘list item’)

`div` Element ohne semantischen Gehalt, nach Möglichkeit vermeiden

`em` betonte Zeichenfolge (Emphase, meist kursiv)

`strong` starke Zeichenfolge (meist fett)

`a` Ankertext, Link

`span` inline Element ohne semantischen Gehalt, nach Möglichkeit vermeiden.

`<!-- -->` Ein Kommentar (wird nicht angezeigt)

## Typische CSS-Eigenschaften und ihre Werte

`margin` Aussenabstand. Angabe in `px`, `rem`.

`margin: 1rem` 1 Wert: oben/unten/links/rechts

`margin: 1rem 2rem;` 2 Werte: oben/unten und links/rechts

`margin: 0 2rem 1rem;` 3 Werte: oben, liks/rechts, unten

`margin: 1rem 1rem 2rem 0;` 4 Werte: von oben im Uhrzeigersinn

`padding` Innenabstand, Werte analog zu `margin`

`font-size` Schriftgrösse, in idealerweise in `rem`. Schriftgrössen in `vw` sind interessant. Die Einheiten `px`, `pt`, `em` und dergleichen solltest du vermeiden.

`line-height` Die Zeilenhöhe (Schriftgrösse + Durchschuss). Angabe als Verhältnis zur Schriftgrösse: `1.3`. Nie in `px` definieren!

`color` Schriftfarbe, als Name `dodgerblue`, als RGB-Wert `rgb(255 0 0)` als Hexadezimalwert `#FF00FF` oder als HSL-Wert `hsl(300 100% 50%)`.

`background-color` oder kurz `color` Hintergrundfarbe, Wert wie Schriftfarbe.

`border` Umrisslinie. Drei Werte für Art, Dicke und Farbe: `solid 1px black`

## Die HTML-Grundstruktur

```
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
  <title>Titel</title>

</head>
<body>
  <h1>Hello World!</h1>
</body>
</html>
```

##  CSS-Regeln

Selektor, gefolgt von Deklaration:

```
p {
  font-size: 0.75rem;
  line-height: 1.2;
}
```

Die Schriftgrösse so einstellen, dass die Benutzereinstellungen respektiert werden.

```
:root {
  font-size: 100%;
  line-height: 1.2;
}

/* Alle weiteren Schriftgrössen mit der Einheit "rem" einstellen. */
```


