# TinkerMario

A pixel-art breadboard trainer — 48 levels that take you from a single lit LED to
Arduino and ESP32 code, built for [Cirkutry](https://github.com/21ss00).

Play it: **https://21ss00.github.io/tinkermario/**

## What's in it

| World | Levels | Covers |
|---|---|---|
| 1 — Breadboard Basics | 10 | complete loops, strips and the ravine, series vs parallel, diodes, capacitors, light sensors |
| 2 — Switching & Logic | 10 | buttons, transistors, and the NOT / AND / OR / XOR / NAND / NOR / XNOR chips |
| 3 — Build Challenges | 10 | multi-chip puzzles: vault locks, interlocks, parity detectors |
| 4 — Arduino Code | 10 | `digitalWrite`, `delay`, sensors, `digitalRead`, state and edge detection |
| 5 — ESP32 Code | 8 | capacitive touch, PWM, RGB strips, combined conditions |

## How it works

The board is simulated as a real breadboard: each column's top half is one electrical
strip, its bottom half is another, and the gap down the middle is why they're separate.
Current has to leave the **+** rail, pass through your parts, and arrive back at **−**
before anything lights — a dead-end branch stays dark no matter how much power reaches it.

Hole colours show where you stand:

- **red** — tied straight to **+**
- **blue** — tied straight to **−**
- **amber** — powered through a load
- **dark** — floating

Code levels run your sketch in a Web Worker on a virtual clock, so an infinite loop
reports back instead of freezing the page.

Everything is one self-contained `index.html` — no build step, no dependencies.
Fonts come from Google Fonts; everything else is inline.
