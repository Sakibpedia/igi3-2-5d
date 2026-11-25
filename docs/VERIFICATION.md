# Verification — IGI 3 2.5D

Godot 4.3 stable, Windows. All commands exited 0.

| Suite | Result |
|---|---|
| `CityTest.tscn` | `[CITY2D] PASS` — 1,500 buildings, 341 roads, 30 shops, 15 gates, 9 vehicles |
| `SaveTest.tscn` | `[SAVE2D] PASS` — 15 missions, wallet, medals, unlocks, save/reload |
| `run_all.ps1` (smoke) | `[IGI2D] ALL 15 MISSIONS PASS` |
| `run_all.ps1 -Deep` | `[PLAY2D] ALL 15 MISSIONS PASS` — real shooting, neutral reactions, airstrikes, shops, interiors, all objectives, extraction |

## Rendering checks

- Menu, mission, interior, shop, BCS gate and result frames were captured from
  the running game with `tools/test/ScreenshotTest.tscn` and saved in
  `docs/images/gameplay-*.png`.
- The first render pass hit a software-renderer crash from too many per-window
  draw calls; window dots were removed and floor bands capped at five per wall,
  after which all six modes rendered without crashes.
- Windows export built and launched successfully.

All mission results are in the 2D/2.5D shared test suite output; the 2.5D edition
uses the same gameplay rules with extruded rendering.

Credit: S M Nazmuz Sakib. Map data © OpenStreetMap contributors (ODbL).
