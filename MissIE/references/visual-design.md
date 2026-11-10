# Shared Visual Grammar (1995–2005)

Use this reference for **style primitives**, not a universal color scheme or layout. The period included utilitarian system-gray programs, bespoke colorful Korean PC utilities, and glossy enterprise-web interfaces. Match the product category and its intended users.

## 1. Surface construction and gradients

- Prefer **vertical, closely related-color gradients** on titles, menus, tabs, headers, toolbars, table headings, and command buttons; normally light at the top, darker at the bottom.
- Use two or three tonal steps, sometimes a more abrupt midpoint to produce a glossy plastic strip; a smooth two-stop gradient suits earlier or subdued systems.
- Add 1px borders, inner highlights, narrow bevels, crisp separators, recessed input borders, and slight hard-edged shadows. Treat borders as structural UI cues.
- Keep reading areas and data grids mostly flat: white, ivory, or light gray. Decorative chrome should frame the content rather than overwhelm it.
- Avoid rainbow gradients, aurora backgrounds, giant radial glows, blur/glassmorphism, oversized soft shadows, and modern translucent floating cards.
- **Do not gradient every surface.** Strong use on chrome and selective use on content titles creates the authentic rhythm.

## 2. Variation, not a fixed skin

Choose independently for each product:

| Design dimension | Period-plausible directions |
| --- | --- |
| Identity | Office-neutral, dark navy, aqua utility, forest green, purple, beige, industrial charcoal |
| Density | Compact desktop utility, moderately dense corporate web form, constrained embedded screen |
| Emphasis | Text/records first; branded bitmap-like graphics first; status/monitoring first |
| Navigation | Menubar, tab strip, left tree, horizontal site nav, segmented utility panel; only what is useful |
| Chrome | Thin plain rules, double-line bevels, lightly glossy headers, strongly graphic vendor-designed modules |

Use user-provided imagery to extract **hierarchy, proportions, gradient direction, icon treatment, and density**. Preserve uniqueness and do not copy an entire reference app.

## 3. Type and spacing

- Model the feel of **Gulim/Dotum (굴림/돋움), Tahoma, Arial, MS Sans Serif**, with locally available and readable fallbacks. Do not bundle proprietary font files or depend on missing system fonts.
- Compact typography and small label-to-title ratios are period-typical, but keep readable sizes, scalable text, sufficient line height, and keyboard focus.
- Prefer explicit panel headings and tight vertical grouping over big bold hero sections, huge metrics, and expansive whitespace.
- A little deliberate compactness is appropriate; illegible 9px data is not a requirement.

## 4. Icons and illustrations

- Favor compact **16x16 / 20x20 / 24x24 / 32x32 filled-color icons**, with outlines, 1px highlights, subtle shading, or a bitmap-era visual rhythm.
- When suitable, pair a medium-sized colorful icon with a short command label on a primary toolbar. Keep small functional icons for rows and tree items.
- SVG and CSS implementations are fine; the rendered visual language should feel bitmap/pixel-drawn. Never require GIF files or deliberately degraded resolution.
- Avoid default monochrome thin-stroke icon kits, decorative emoji, or modern illustration mascots. If a project already uses a modern icon library, restyle/replace the **visible result**, not necessarily its dependency.
- Do not reuse third-party logos, copyrighted program graphics, or trademarks without authorization.

## 5. Example primitives (illustration, not mandatory colors)

```css
:root {
  --frame-edge: #8da4b6;
  --inner-light: #f7fbfe;
  --surface: #f0f3f6;
  --section-gradient: linear-gradient(180deg, #f8fbfd, #d9e7f1 52%, #b8cfdf);
  --button-gradient: linear-gradient(180deg, #ffffff, #e9f1f6 48%, #ccdae5);
  --nav-gradient: linear-gradient(180deg, #7ea9cf, #2d6ea7 49%, #205a92 50%, #3d79ad);
}
.legacy-section-heading {
  background: var(--section-gradient);
  border: 1px solid var(--frame-edge);
  box-shadow: inset 0 1px 0 var(--inner-light);
}
.legacy-command {
  background: var(--button-gradient);
  border: 1px solid var(--frame-edge);
  border-radius: 0;
  box-shadow: inset 1px 1px 0 #fff;
}
```

The values are *example mechanisms*, not shared mandatory constants. Recalculate contrast and adapt color/density to the specific app.

## 6. Distinguish authentic period styling from weak cosplay

| Avoid | Prefer |
| --- | --- |
| Modern SaaS cards with `border-radius: 0` | Task-based screen structure with commands, title strips, forms, grids and status |
| Fake OS desktop and giant window frame in every web page | The actual web or application conventions for its platform |
| Every screen colored corporate blue | Independent vendor identity, with period-appropriate shading |
| Gradient-covered content and large 3D ornaments | Gradients concentrated on actionable chrome, plain data regions |
| Pixelation that harms comprehension | Clear modern vectors/CSS shaped in bitmap-era idiom |
| Vague animated spinners | Explicit loading/processing state; measurable percentage only when known |

## 7. Visual acceptance check

A successful screen should communicate the era at first glance through **composition, control styling, icons, and language together**. If only the colors look retro but the skeleton is a modern dashboard, redesign the skeleton.
