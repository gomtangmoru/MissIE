# Web Interfaces — Korean Enterprise / Classic Web (1998–2005)

Use this reference for browser-based applications: login screens, internal portals, groupware, CMS, ERP, early web dashboards, online management systems, and administration pages. The target is **old web application design**, not a Win32 desktop inside a web browser.

## Distinct web lineages

1. **Corporate intranet / groupware (1999–2005):** branded top header, compact utility links, top navigation, side modules, notice board, search/results, gentle to strong blue/teal/green gradients.
2. **Legacy CMS and administration (1998–2005):** tabular content, narrow title bars, explicit menu hierarchy, low-decoration or lightly beveled controls, data-entry forms.
3. **Professional operations portal (2001–2005):** system name/version, breadcrumbs or path labels, section/toolbar gradients, filters, record grids, operation/status notices.
4. **Vendor-branded utility web UI (2001–2005):** more graphic headers, colorful filled icons, strong menu strips; still task-oriented and compact.

Mix these lineages as justified; **never turn them into four immutable templates**. The result should not always have a blue left sidebar.

## Information architecture

- Design around a **task route** such as `menu -> search criteria -> result list -> item detail -> update/apply`. For simpler apps, use only the necessary steps.
- Header may include logo, product name, user/session name, login/logout, help, and product/version links **only where they are real and appropriate**.
- Use optional top navigation, small text utilities, breadcrumb/current-location text, tabs, and side navigation. Do not force all of them into every page.
- Search/filter panels use clearly labeled form controls, compact dropdowns, date fields, and a visible `조회`/Search command when relevant.
- Lists rely on **data tables, category trees, compact status cells, and inline action links** where they improve comprehension. Use proper semantic HTML tables for tabular data, not obsolete layout tables.
- Announcements, notice sections, help links, and labeled status strips can establish an authentic portal feel when they fit the content. Avoid inventing historical notices or fictitious maintenance alerts as if factual.
- For charts, favor framed plot areas, small legends, axis labels, solid/stepped lines and basic fills; do not require old charting software or fabricate measurements.

## Concrete visual details

- Use a **full-width narrow horizontal strip** for page titles or section headers, often with a vertical gradient, 1px keyline, and a small icon or marker at the left.
- Use compact boxed controls, solid borders, striped or ruled grid tables, simple pagination (`처음 / 이전 / 1 2 3 / 다음 / 끝`) when useful.
- Let body backgrounds remain plain; different shades of the same color can subtly separate search, grid, and side-navigation blocks.
- Small site-brand artwork, glossy horizontal navigation, dotted rules, and period-shaped filled icons are welcome. Larger graphics should not displace key tasks.
- Fixed-width visual proportions are allowed as **an aesthetic**, but implement with modern flexible or responsive layout. Do not introduce horizontal overflow at common viewport sizes.

## Login page pattern

An authentic login page may feature a corporate logo and product title, graduated header or navigation strip, username/password fields, a compact authentication box, a notice list, and system/help links. However:

- Do not automatically add an entire dashboard navigation or a fake desktop taskbar to the login screen.
- Use a real form with appropriate labels, password input type, password-manager compatibility, Enter-to-submit, and visible validation feedback.
- Follow real authentication/session/CSRF/rate-limit requirements of the existing project. Never reproduce unsafe 2000s login behavior.
- Do not display a fictional successful authentication, verified security certification, live system status, corporate identity, support phone, or error code without evidence.
- If the task is visual-only, say that authentication is not wired; a demo interaction must not pretend to log in.
- The page should communicate an official system, not a welcoming conversational onboarding assistant.

## Copy and states

- For Korean, read `korean-localization.md`. Prefer `사용자 ID`, `암호`, `접속`, `로그인`, `자료 조회`, `조회 결과`, `등록`, `환경 설정`, `이용 안내` where context supports them.
- Give distinct pending, empty, error and completed states. Error details should describe **real** validation/connection failures; loading or progress must not be fictional.
- Announce form errors accessibly; do not rely on color alone.

## Do not revive obsolete technology

Use React, Vue, Svelte, modern CSS, semantic HTML and accessible widgets as appropriate. Do **not** use framesets, ActiveX, Flash, browser sniffing, insecure auth, image-only text, tiny fixed pixel fonts, or dependency on Internet Explorer. Nostalgia should appear in the rendered UI, not the technology stack.

## Failure-mode check

- If it looks like a modern startup's dashboard with retro borders, restructure for a period-appropriate web workflow.
- If it looks like a desktop OS window embedded in the page, replace fake chrome with actual period web navigation and panel structure.
- If every section uses glossy gradients, restore contrast through flatter reading/data surfaces.
- If the UI resembles a single reference site too closely, introduce product-specific palette, composition and graphics while preserving the era.
