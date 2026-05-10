1. General Principles
Follow consistency over personal preference.
Avoid duplication — reuse classes and patterns.
Styles must be predictable and easy to override.
2. File & Structure

Use a clear structure inside CSS file:

/* Base / Reset */
/* Variables */
/* Layout */
/* Components */
/* Utilities */
Keep related styles grouped together.
Avoid хаотичного порядку селекторів.
3. Naming Convention

Use kebab-case:

.main-header {}
.footer-link {}
Use meaningful names:
❌ .box, .item
✅ .product-card, .nav-link
Avoid styling by tag:
❌ div {}
✅ .card {}
4. Specificity & Selectors
Keep specificity low.

Avoid nesting deeper than 2–3 levels:

/* ❌ */
.header .nav .list .item a {}

/* ✅ */
.nav-link {}
Do not use !important (except extreme cases).
5. Layout Rules
Prefer modern layout systems:
flexbox
grid
Avoid outdated techniques:
❌ float
Use gap instead of margins for spacing in flex/grid.
6. Units & Sizing
Use relative units:
rem, em, %
Avoid excessive use of px (except borders, shadows)
Do not mix inconsistent units in one component
7. Colors & Variables

Use CSS variables:

:root {
  --primary-color: #ff6b6b;
}
Do not repeat hardcoded colors multiple times
Maintain a consistent color palette
8. Typography

Define base font styles:

body {
  font-family: sans-serif;
}
Use consistent font sizes (prefer scale system)
Avoid random font-size values
9. Spacing System
Use consistent spacing scale:
4px / 8px system recommended
Avoid random margins/paddings:
❌ margin: 13px
✅ margin: 16px
10. Reusability

Extract reusable classes:

.btn {}
.btn-primary {}
Avoid duplicating identical styles
11. Responsiveness

Use media queries:

@media (max-width: 768px) {}
Mobile-first approach preferred
Avoid fixed widths where possible
12. Clean Code
Remove unused styles
No commented-out dead code

Keep formatting consistent:

.class {
  display: flex;
  align-items: center;
}
13. Performance
Avoid overly complex selectors
Minimize reflows and repaints
Keep CSS lightweight
14. Validation & Standards
CSS must be valid (no broken properties)
Avoid vendor prefixes unless necessary
Follow modern CSS standards


## Strict Mode

- Any duplication = warning
- Any !important = error
- Deep nesting (3+) = warning
- Hardcoded colors (without variables) = warning
- Non-semantic naming = warning