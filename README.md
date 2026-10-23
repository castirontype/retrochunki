# RetroChunki

A sixteen-segment illuminated-display face, drawn after the lamp cell of
F. W. Wood's 1910 patent 974,943, "Illuminated Announcement and Display
Signal" (filed 1908, assigned to Charles Cory & Son of New York).

## The lamp cell

Wood was not drawing type. He was building a shipboard signal light: a bank
of lamps behind ground glass, wired so a gunner could read range, deflection
and a handful of fixed orders ("CEASE", "COMMENCE") from across a deck. The
part worth taking is the shape of one lamp cell: "the end of each lamp
compartment or cell is shaped to form an elongated rectangle having pointed
ends, said ends being symmetrically fitted together at each corner." A lens,
not a stadium. The point is sharp, so two cells sharing a corner come to the
same vertex instead of leaving a rounded gap between two rounded caps.

Wood's own monogram is eight of these cells, enough for any digit but not
for a legible Latin letter. This font keeps the lens and uses the
sixteen-segment grid a full alphabet needs. The cell is Wood's. The layout
is common to every 16-segment display ever built. No claim is made that
this is a reproduction of anything Wood built or drew.

## The grid

```
  TL --A1-- TM --A2-- TR
  |  \      |      /  |
  F   H     I     J   B
  |      \  |  /      |
  ML--G1--MM--G2------MR
  |      /  |  \      |
  E   K     L     M   C
  |  /      |      \  |
  BL --D1-- BM --D2-- BR
```

Straight segments are bars with a 45-degree point at each end, so points
meeting at a node face each other across one even seam. Diagonals fill the
box left in each quadrant, cut flat and parallel to the segments they face.

Punctuation sits on a narrow cell of its own, one column of six lamps, the
way a real module carries its decimal point and clock colon. The math
operators `+ − %` sit on a third cell: eight lamps around a centre node.

Some letters are unavoidably close to a digit on any 16-segment grid. `S`
and `5` are the identical segment set here, as they are on a real display;
`B` and `8` differ by one segment. Context disambiguates.

## Character set

A-Z, 0-9, space, `! % ' ’ * + , - . / : ; −` (U+2212 minus). A segment
display has never had a lowercase, and neither does this font.

## Styles

- **`wght` 300-700.** Moves the thickness of every lit cell; weight here
  means a lit cell fills more of its own lens.
- **`slnt` 0-12.** Many real segment displays are built with a lean. Shears
  every glyph about its own baseline.

Static instances: Light, Regular, Medium, Bold, Slanted.

## Features

- **`ss01` Unlit.** Swaps each glyph for the segments it leaves dark, for
  setting a "powered-off" layer under the lit text in a second colour.
- **`ss02` Proportional.** Crops each glyph to its own ink with even air on
  either side, so a word sets at one gap between letters instead of one
  fixed pitch per cell. Off by default: the fixed cell is what a display is.

```css
.lit   { font-family: "RetroChunki"; color: #ff3b2f; }
.unlit { font-family: "RetroChunki"; color: #2a1614; font-feature-settings: "ss01"; }
```

## Files

```
fonts/
  variable/   RetroChunki[slnt,wght].ttf
  ttf/        static TrueType, one per instance
  otf/        static CFF OpenType, one per instance
  webfonts/   woff2 and fonts.css
OFL.txt       license
```

## License

Copyright 2026 Durable Programming, LLC. RetroChunki is licensed under the
[SIL Open Font License, Version 1.1](OFL.txt).

Published by [Cast Iron Type](https://castirontype.com). Designed by
David J Berube.
