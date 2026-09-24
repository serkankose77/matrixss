# matrixss

A set of home pages displaying time and date in front of animated backgrounds. `index.html` loads one of them at random.

## Random selector (`index.html`)

- Loads one of the pages listed in `PAGES` into a full-screen iframe.
- Shuffle bag (kept in `localStorage`): every page is shown once before any page repeats, and the same page never comes up twice in a row.
- Force a specific page with `?p=13`, `?page=index13.html` or `#13`.
- Keyboard focus is handed to the loaded page, so its shortcuts work immediately.

To add a page: create `indexN.html`, append it to `PAGES` in `index.html` and to `pages` in `gallery.html`, and bump `PAGES` in `index16.html` so the terminal's `ls` / `open` commands know about it.

## Pages

`gallery.html` shows every page as a live thumbnail grid.

| Page | Theme |
|---|---|
| `index1` | Matrix digital rain |
| `index2` | Synthwave night drive '84 |
| `index3` | Hyperspace warp |
| `index4` | Aurora borealis (WebGL) |
| `index5` | Terminal boot (tty1) |
| `index6` | Deep ocean abyss |
| `index7` | Spiral galaxy NGC-77 |
| `index8` | Rain on glass |
| `index9` | Firefly forest |
| `index10` | Liquid plasma (WebGL) |
| `index11` | Carta caelestis star chart |
| `index12` | VHS glitch |
| `index13` – `index17` | Interactive pages, see below |

### Interactive pages

| Page | What it is | Controls |
|---|---|---|
| `index13` | Real-time GPU fluid: WebGL stable fluids (semi-Lagrangian advection, vorticity confinement, Jacobi pressure projection) with bloom | move / drag = stir, click = burst, `Space` = splash, `C` = palette, `B` = bloom, `P` = pause |
| `index14` | Particle clock: the title and `HH:MM:SS` are built from spring-bound particles; only the digit that changes re-forms | move = push, hold = charge a vortex / release = shockwave, `Space` = explode, `G` or double-click = gravity, `C` = colors |
| `index15` | CNC engraver: top view of a 3-axis VMC that engraves the time into a 320 x 180 mm 6061 plate, faces it off and re-engraves it every minute. Live G-code listing, DRO, spindle load, chips, tool changes (T1 V-bit / T2 face mill) | drag on the plate = programme a toolpath (becomes G0/G1 moves), click = spot drill (G81), wheel or FEED +/- = feed override, `Space` = feed hold / cycle start, `F` = face the plate, `T` = engrave the time, `E` = E-stop, `S` = spindle sound |
| `index16` | Interactive Matrix rain with a terminal | type commands (`help`, `red`, `blue`, `rainbow`, `cnc`, `echo <text>`, `speed 2`, `ls`, `open 5`, `random`, ...), hold = bullet time, click = shockwave, wheel = speed, `Esc` = hide the terminal |
| `index17` | Density-wave spiral galaxy (Three.js, ~36k stars) with Newtonian black holes that perturb orbits, eat stars, spiral in and merge | drag = orbit, wheel / pinch = zoom, click = drop a black hole, shift+click or long-press = supernova, `C` = clear, `R` = new galaxy, `Space` = pause, `+` / `-` = time scale |
