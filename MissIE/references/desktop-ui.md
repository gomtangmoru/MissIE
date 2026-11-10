# Desktop & Embedded Applications — 1995–2005

Use this reference for desktop-like tools and dedicated interfaces: Win32/Visual C++/MFC, Java AWT/Swing, Windows CE utilities, PDA/industrial terminals, PC diagnostics, download managers, security programs, and vendor-branded standalone software. Reproduce **application conventions**, not the whole operating system.

## Pick the appropriate family

| Family | Typical attributes | Suitable tasks |
| --- | --- | --- |
| Classic native utility (1995–2001) | Neutral controls; menubar, toolbar, tree/list split, group boxes, status bar; obvious selection and focus | File managers, settings, editors, diagnostic tools |
| Java Swing / early Java GUI (1997–2005) | Raised/recessed widget borders, dense panes, label-heavy forms, tables, configuration dialogs | Cross-platform management tools and data editors |
| Windows CE / embedded (1997–2005) | Constrained screens, status/connection indicators, large primary operations, tab/form flows | Instrument panels, PDA utilities, vehicle/industrial controls |
| Branded commercial PC utility (2000–2005) | Graphic product banner, vendor-specific high-contrast palette, vivid vertical gradients, filled shaded toolbar icons, boxed inner panels | Security, download, maintenance, multimedia utilities |

Families can overlap. For example, a 2003 native utility may use both MFC-style settings dialogs and a distinctive, glossy blue-green home screen. Avoid forcing every tool into a bland gray Windows 95 look.

## Components and behavior

- Use, where appropriate, `File / Edit / View / Tools / Help` menus, toolbar commands, tabs, group boxes, item trees, list views, property grids, split panes, message dialogs, and status bars.
- Keep tasks explicit: `Open`, `Search`, `Register`, `Modify`, `Delete`, `Save`, `Apply`, `Cancel`, `Refresh`, `Properties`, `Help`.
- Prefer explicit selection, rows, column headers, in-place property editing where appropriate, and clear disabled/checked/selected states.
- Keep `OK`, `Cancel`, and `Apply` semantically distinct: `Apply` can persist in place; `OK` accepts and closes; `Cancel` should not silently persist uncommitted changes.
- Add double-click or context menus only if meaningful, with keyboard equivalents wherever feasible. Map `Enter`, `Esc`, `Tab`, `F1` and accelerator keys **only if supported**; don't print fake shortcut labels.
- The status bar can show a selected item count, current activity, connection state, or last operation result when actually known.

## Embedded / CE guidance

- Constrained space should produce clear, prioritized control surfaces and concise status, not intentionally microscopic text.
- For touch-oriented equipment, provide usable hit targets regardless of old visual styling.
- Show actionable device state and communication state when available, distinguish `offline`, `connecting`, `ready`, and `failure`; never synthesize live telemetry.
- Avoid web dashboard conventions such as huge marketing KPI cards and endless scroll as the default interaction model.

## Graphic commercial utility guidance

- Product-specific illustrations, reflective headers, a gradient sidebar or ribbon-like command section, and bright small artwork are plausible for early-2000s third-party software.
- Use graphics to establish hierarchy, not distract from an ordinary file or settings form. A strong header can coexist with otherwise classic raised controls and small data tables.
- Keep the product visually distinct; avoid cloned Windows XP Luna themes and generic Windows-looking fake titlebars everywhere.

## Error and progress behavior

- Distinguish `ready`, `in progress`, `completed`, and `failed` states.
- Display percentage only when a real measurable total exists; otherwise use an indeterminate indicator plus a specific operation label.
- In technical utilities, offer error details/logs when available. Do not fabricate Win32 error numbers or network diagnostics.
- Prevent destructive actions from being casually executed; explicit confirmation and recoverability take precedence over visual nostalgia.
- Read `korean-localization.md` for Korean system labels and authentic imperative/error phrasing.

## Implementation boundaries

Use the user's current stack (Electron, Tauri, Qt, .NET, Java, web-in-desktop, etc.). Re-theme current controls or compose accessible new ones, but **do not downgrade libraries, disable security, or introduce unmaintained GUI frameworks solely for appearance**. If a program must work on modern high-DPI displays, scale graphics and typography cleanly.
