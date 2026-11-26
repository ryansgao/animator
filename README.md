# Animator

A web app for animating line drawings described by small Gleam programs, built for CS 61A (Fall 2026).
The app includes an interpreter for a subset of Gleam that runs entirely in the browser.

Live: https://ryansgao.github.io/animator/ — opens on the "bloom" drawing; the menu has presets
(bloom, handwriting, spirograph, title card, then the original examples) to try the extension straight away.

## Extension: handwriting, curves and colour

- `Text(at, "text", size)` writes words on the canvas stroke by stroke, in a single-stroke font made for the app.
  Strings are part of the language (lists of character codes), with `<>` to join them and `show(n)` for numbers.
- `Arc(center, radius, from, to)` and `Curve(start, control, end)` draw round shapes, animated along their length.
- `Tint(shape, hue)` draws any shape in a chosen colour; `sin` and `cos` place points around a circle.
