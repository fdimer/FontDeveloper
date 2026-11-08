# Font Developer

A personal tool for designing fonts. Draw each character on the left, see the result
on the right, and export a TrueType font (`.ttf`).

## Running

Open `index.html` in a browser. There's nothing to install and no network access.

## Drawing

| Tool | Key | Use |
|---|---|---|
| Pixel | P | Left button paints grid cells, right button erases |
| Erase | E | Erase grid cells |
| Line | L | Press, drag, release |
| Arc | A | Drag from start to end, release, move to bend, click |
| Select | V | Click a line or arc to move it, drag its handles to reshape, Delete removes it, drag the dashed line to set the character's width |

Other keys: Ctrl+Z / Ctrl+Y undo/redo, Ctrl+S save project, Page Up / Page Down change character, Esc cancels.

Stroke width and line ends apply to new shapes, and to the selected shape when changed.
Shapes and pixels can be mixed in one character; overlaps merge.

## Files

- **Save project** writes `<name>.fontdev.json` (all drawings and settings). **Open…** loads it.
  Work is also kept automatically in the browser between sessions.
- **Export .ttf** writes a TrueType font with every character that has a drawing, plus space.

## Code

- `js/ttf.js` — TrueType writer (no dependencies)
- `js/outline.js` — turns pixels, lines and arcs into outlines (shared by the editor, preview and export)
- `js/app.js` — the editor and preview

## Licence

MIT, see [LICENSE](LICENSE).
