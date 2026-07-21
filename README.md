# Senyatyl Layout Editor

Single-file visual editor for Senyatyl key geometry.

Live version:

https://senyasdt.github.io/senyatyl-layout-editor/

Open `index.html` in a browser. No build step is required.

## What It Edits

The editor keeps one internal key list and exports both files used by the ZMK repo:

- `config/boards/shields/senyatyl/senyatyl.dtsi`: paste the `DTSI keys` block into `physical_layout_0.keys`.
- `config/senyatyl.json`: replace the whole file with the `Keymap Editor JSON` output.

The JSON `row` and `col` fields are visual positions for Nick Coutsos' Keymap Editor. They are not ZMK matrix row/column pins.

## Controls

- Drag a key to move it.
- Arrow keys move the selected key by 1 unit.
- Shift + arrow moves by 10 units.
- `Q` / `E` rotate by 1 degree.
- Shift + `Q` / `E` rotate by 5 degrees.
- `Snap 10` rounds key positions to a 10-unit grid.
- `Tighten 5%` compresses all key positions toward the top-left origin.

## Import

Paste an existing DTSI `keys` block into `DTSI keys` and click `Import DTSI textarea`.

Paste an existing `senyatyl.json` into `Keymap Editor JSON` and click `Import JSON textarea`.

You can also import automatically:

- Click `Import JSON/DTSI file` and choose a `.json`, `.dtsi`, `.overlay`, or `.txt` file.
- Drag and drop a JSON/DTSI file onto the page.
- Paste JSON or a DTSI keys block into either textarea.
