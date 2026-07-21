# Keyboard Layout Editor

Single-file visual editor for ZMK physical layout geometry and Keymap Editor JSON.

Live version:

https://senyasdt.github.io/senyatyl-layout-editor/

Open `index.html` in a browser. No build step is required.

## What It Edits

The editor keeps one internal key list and exports both layout formats:

- ZMK DTSI `physical_layout_0.keys` blocks using `key_physical_attrs`.
- Nick Coutsos Keymap Editor JSON files.

The bundled starting layout is Senyatyl, but imported JSON/DTSI files can have any key count.

The JSON `row` and `col` fields are visual positions for Keymap Editor formatting. They are not ZMK matrix row/column pins.

## Controls

- Drag a key to move it.
- Arrow keys move the selected key by 1 unit.
- Shift + arrow moves by 10 units.
- `Q` / `E` rotate by 1 degree.
- Shift + `Q` / `E` rotate by 5 degrees.
- `Add key` adds a key next to the selected key.
- `Delete key` removes the selected key.
- `Infer row/col` recalculates JSON row/column values from current geometry.
- `Snap 10` rounds key positions to a 10-unit grid.
- `Tighten 5%` compresses all key positions toward the top-left origin.

## Import

Paste an existing DTSI `keys` block into `DTSI keys` and click `Import DTSI textarea`.

Paste an existing Keymap Editor JSON into `Keymap Editor JSON` and click `Import JSON textarea`.

You can also import automatically:

- Click `Import JSON/DTSI file` and choose a `.json`, `.dtsi`, `.overlay`, or `.txt` file.
- Drag and drop a JSON/DTSI file onto the page.
- Paste JSON or a DTSI keys block into either textarea.
