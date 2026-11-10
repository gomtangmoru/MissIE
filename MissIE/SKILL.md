---
name: MissIE
description: MissIE brings back the look and feel of 1995–2005 software
  using modern technologies. Recreate classic Windows, Win32,
  MFC, Java Swing, Windows CE, and early web application
  aesthetics, including beveled controls, gradient headers,
  bitmap-style icons, dense layouts, and formal system messages.
  Preserve authentic legacy UI/UX conventions without sacrificing
  modern functionality, accessibility, or performance.
  Activate this skill whenever the user asks for retro, vintage,
  1995-2005, Windows 95/2000/XP, Win32, classic web, or 2000s
  Korean enterprise/intranet aesthetic, or calls /MissIE or $MissIE.
---

# MissIE

Create software that **looks and communicates like a product designed in 1995–2005**, while using the project's current frameworks, security practices, and accessible interaction patterns. The goal is **period-authentic product design**, not a mock Windows desktop or a modern SaaS page with gray CSS.

## Scope and precedence

- Apply to new UI and UI redesigns when this skill is selected. Do not impose a retro redesign on backend-only changes.
- Follow the user's explicit style, references, scope, locale, and existing product identity before this skill's defaults. Do not clone a named product, trademark, or supplied image verbatim unless explicitly authorized.
- Target 1995–2005 design conventions. Later products may inform the work only when their visual language clearly belongs to this period. Avoid Vista/Aero, contemporary mobile design, and modern flat/SaaS defaults.
- Preserve the existing stack and functional behavior. No ActiveX, Flash, deprecated security practices, fabricated status values, or intentionally broken usability.
- Choose a **distinct visual identity for each product**. Do not require the same blue header, sidebar, fixed-width layout, or pixel-perfect template everywhere.

## Read only the relevant references

Use the following local files as **selective guidance**, not as material to load automatically in full:

| Task | Read |
| --- | --- |
| Any visual UI design or restyling | `references/visual-design.md` |
| Websites, login pages, intranets, groupware, CMS, ERP, web dashboards | `references/web-ui.md` |
| Native desktop utilities, MFC/Win32/Swing-like apps, embedded or Windows CE-like tools | `references/desktop-ui.md` |
| Korean UI labels, instructions, dialogs, errors, notifications or help text | `references/korean-localization.md` |

For hybrid applications, read both platform references. For English-only interfaces, apply the language principles in this file without loading the Korean-specific examples unless useful.

## Design procedure

1. **Inspect context.** Identify existing components, routes, UX constraints, brand, viewport, and task workflows. Honor a provided reference image's *design grammar*, not merely its colors.
2. **Pick the period-appropriate lineage.** Choose or mix classic native utility (1995–2001), branded PC utility (2000–2005), Windows CE/embedded (1997–2005), Korean enterprise web (1998–2005), or early professional web console (2001–2005). Never treat these as fixed templates.
3. **Define visual rules before implementing.** Choose a project-specific palette, vertical gradients for selected interface chrome, 1px edges/bevels, compact information hierarchy, period-plausible icons, and typography. Design the layout around tasks and data rather than modern marketing cards.
4. **Build the actual workflow.** Choose familiar controls (menus, tabs, toolbars, tree/list views, dense forms, tables, properties, wizard dialogs, status bars) only when justified by the product. Provide explicit commands such as Search, Register, Apply, Save, Cancel, and Refresh.
5. **Write period-appropriate UI copy.** The program issues concise instructions and reports status/results; it does not chat, praise, or anthropomorphize itself. When Korean is used, follow `references/korean-localization.md`.
6. **Validate implementation.** Test real interactions, pending/success/error/empty states, keyboard controls, responsive fallback, accessible names, contrast, current functionality, and the project's build/tests where available.

## Non-negotiable behaviors

- **Period authenticity over visual uniformity:** do not force identical colors, menus, or components across unrelated projects.
- **Task-first, not hospitality-first:** system messages should say what happened, what is happening, or what the user must do. Avoid conversational encouragement and oversized welcome sections.
- **Graphic chrome, restrained content:** period-typical vertical gradients and bevels belong primarily on banners, section headers, tabs, toolbars, buttons, and navigation; keep data/content surfaces comparatively plain.
- **Real behavior only:** do not invent error codes, progress percentages, latency, server health, versions, dates, or successful authentication. Do not advertise a keyboard shortcut unless implemented.
- **No nostalgia at the cost of quality:** maintain current security, accessibility, scalable text, sensible touch targets where applicable, and modern framework conventions. Avoid deprecated browser APIs and insecure implementations.
- **No irrelevant window chrome:** web pages should resemble period websites, not windows pasted into the browser; desktop software should resemble applications, not SaaS dashboards.

## Finish-line check

- Would this plausibly look like a **distinct** commercial or internal software product made in 1995–2005?
- Are title/header gradients, sharp edges, icon style, information density, and typography coherent without copying a universal template?
- Are every visible label, dialog, status, error, and command period-appropriate for the UI's language?
- Is the result more than a modern card dashboard with retro colors?
- Do controls work and report truthful states? Are accessibility, responsiveness, and security intact?

**Design test:** *What would a 1995–2005 software company build with its design sensibilities if it had today's implementation tools?*
