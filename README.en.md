# JSON Interface

Two standalone HTML editors to load, edit, and download JSON files. Each file is self-contained (HTML + CSS + JS inline), with no external dependencies.

---

## 1. `editor-json.html` — Form editor

**Title:** Interactive JSON Editor  
**Use:** Form view, suitable for any device; compact layout on desktop with label and field on the same row.

### Features

- **Loading:** Choose a `.json` file or use **Load example** for sample JSON.
- **Editing:** Fields are generated automatically from the JSON:
  - **Strings, numbers, booleans** → input fields (text, number, checkbox).
  - **Objects** → collapsible/expandable blocks with nested fields.
  - **Arrays** → object arrays with add/remove rows; primitive arrays with search and dropdown selection.
- **Collapse / Expand:**  
  - **Collapse all** and **Expand all** at the top of the editor.  
  - Each object/array (and each item in object arrays) can be collapsed/expanded by clicking the title row (triangle ▼/▶).
- **Add / Remove (top level only):**
  - **+** (green): At the bottom of the form, in the “New field” row. Adds a new top-level field with the **same structure** as the first existing field (object, array, or primitive). Optional: type the key name in the text field.
  - **−** (red): On each **top-level** row, removes that field from the object (data updated and form re-rendered).
- **Preview:** Live JSON preview below the form.
- **Download JSON:** **Download JSON** button to save the modified JSON.

### How to use

Open `editor-json.html` in a browser (file:// is fine). No server required.  
A copy is also available at `json/editor-json.html` (same features).

---

## 2. `editor-json-tabella.html` — Table editor (desktop)

**Title:** JSON Editor – Table view (PC)  
**Use:** Horizontal table layout, aimed at large screens.

### Features

- **Loading:** Same as the form editor: JSON file or **Load example**.
- **Table editing:**  
  - **Objects** are shown as tables (keys as columns, values in editable cells).  
  - **Arrays** as bullet lists or tables; **+** / **−** buttons to add or remove rows/items.  
  - Cells use `textarea` with line wrap; minimum height and preview when a row is collapsed.
- **Collapse / Expand:** Global and per-row collapse/expand.
- **Preview and download:** JSON preview and **Download JSON** to save the modified file.

### How to use

Open `editor-json-tabella.html` in a browser. Best used on desktop to take advantage of the table layout.

---

## Summary

| File                      | View   | Best for           | Notes                                           |
|---------------------------|--------|--------------------|-------------------------------------------------|
| `editor-json.html`        | Form   | All devices        | Label and field on same row; +/− at top level only |
| `editor-json-tabella.html`| Table  | Desktop / PC       | Objects in tables, arrays as rows/lists        |

Both files have a UI in Italian and require no installation: just open them from the filesystem.
