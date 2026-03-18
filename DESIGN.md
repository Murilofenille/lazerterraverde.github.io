# Design System Document: Editorial Leisure & Horizon

## 1. Overview & Creative North Star

### The Creative North Star: "The Modern Estate"
This design system is built to evoke the feeling of a high-end, architectural retreat. We are moving away from the "booking app" cliché of heavy borders and cluttered grids. Instead, we embrace **Organic Editorialism**—a style characterized by vast breathing room, sophisticated tonal layering, and intentional asymmetry that mimics the layout of a luxury lifestyle magazine.

The goal is to transition the user from the "task" of renting to the "experience" of the space. We achieve this through:
*   **Intentional Asymmetry:** Breaking the vertical rhythm with overlapping imagery and offset typography.
*   **Tonal Depth:** Replacing structural lines with soft shifts in background colors to define zones.
*   **High-Contrast Scale:** Using oversized `display` typography against delicate `body` text to create an authoritative yet relaxed visual hierarchy.

---

## 2. Colors

The palette is a sophisticated mix of botanical greens and coastal blues, anchored by a warm, paper-like cream.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to section off content. Boundaries must be defined solely through background color shifts. For example, a `surface-container-low` section should sit directly against a `surface` background to create a soft, edge-less transition.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine paper. Use the following tiers to create depth without shadows:
*   **Base Layer:** `surface` (#fff8f0) – Use for the primary page background.
*   **Low Elevation:** `surface-container-low` (#faf3e8) – Use for secondary content areas or large section blocks.
*   **High Elevation:** `surface-container-highest` (#e8e2d7) – Use for interactive "cards" or "floating" elements to make them pop against the base.

### Glass & Gradient (The Soul of the UI)
To avoid a flat, "out-of-the-box" appearance:
*   **Glassmorphism:** Use `surface-container-lowest` at 80% opacity with a `20px` backdrop-blur for navigation bars and floating action menus.
*   **Signature Gradients:** Use a subtle linear gradient (Top-Down: `primary` to `primary-container`) for Hero backgrounds. This provides a lush, deep forest feel that flat hex codes cannot replicate.

---

## 3. Typography

The typography strategy pairs the geometric precision of **Plus Jakarta Sans** for headers with the approachable clarity of **Manrope** for utility.

*   **Display (Plus Jakarta Sans):** These are your "Editorial Hooks." Use `display-lg` for hero statements. The generous tracking and large scale convey premium quality.
*   **Headline & Title (Plus Jakarta Sans):** Used for sectioning. Keep these high-contrast against the cream backgrounds.
*   **Body (Manrope):** Set in `body-lg` or `body-md`. Manrope provides a modern, clean look that ensures legibility for rental details and terms.
*   **Labels (Manrope):** Small, all-caps or high-weight utility text.

**Hierarchy Note:** Always ensure a minimum of 2 size steps between a Headline and Body text to maintain the editorial "staggered" look.

---

## 4. Elevation & Depth

We eschew traditional "Box Shadows" in favor of **Tonal Layering**.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section. This creates a natural "lift" that mimics high-quality stationary.
*   **Ambient Shadows:** If a floating element (like a "Book Now" bar) requires a shadow, it must be an "Ambient Shadow": `0px 20px 40px rgba(30, 27, 21, 0.06)`. The color is a tint of our `on-surface` color, never pure black.
*   **The Ghost Border:** If a border is required for accessibility (e.g., input fields), use `outline-variant` at 20% opacity. **Never use 100% opaque borders.**
*   **Glassmorphism:** Floating modals or dropdowns should utilize a semi-transparent `surface` with a heavy blur to integrate into the lush green/blue backgrounds of the leisure photography.

---

## 5. Components

### Buttons: The Primary Anchor
Buttons must be prominent but sophisticated.
*   **Primary:** Background: `primary` (#004633); Text: `on-primary` (#ffffff). Shape: `md` (0.75rem) or `full`.
*   **Secondary:** Background: `secondary-container` (#97cffe); Text: `on-secondary-container` (#165981).
*   **Tertiary (The "Lime" Pop):** Use the `tertiary-fixed` (#ccf15f) for high-conversion CTAs. It acts as a visual spotlight.

### Cards & Lists: The "No-Divider" Rule
*   **Forbid Divider Lines:** Never use a horizontal line to separate list items. Instead, use the **Spacing Scale** (e.g., `8` or `10`) to provide breathing room.
*   **Card Styling:** No borders. Use `surface-container-highest` backgrounds with a corner radius of `xl` (1.5rem) to reflect the organic, "leisure" feel of the logo.

### Input Fields
*   **Style:** Minimalist. Use a `surface-container-low` background with a `sm` (0.25rem) corner radius. Use `label-md` for floating labels.
*   **Active State:** Transition the "Ghost Border" from 20% to 100% `primary` color.

### Signature Component: The "Leisure Carousel"
A bespoke component for browsing pools or deck areas. Use asymmetric card sizes (e.g., one large `surface-container` card followed by two smaller ones) to prevent the layout from feeling like a standard grid.

---

## 6. Do's and Don'ts

### Do:
*   **DO** use whitespace as a functional element. If in doubt, increase the spacing to the next tier in the scale.
*   **DO** use the Deep Blue (`secondary`) for "Professional" elements (terms, contact info) and Deep Green (`primary`) for "Leisure" elements (amenities, booking).
*   **DO** use high-quality photography that bleeds off the edge of the screen to create an immersive "resort" feel.

### Don't:
*   **DON'T** use 1px black or grey borders. They break the premium illusion and make the UI look like a template.
*   **DON'T** use standard Material Design "Drop Shadows." They are too heavy for this breezy, light-filled brand identity.
*   **DON'T** crowd the display typography. If a headline is `display-lg`, it needs at least `40` (7rem) of vertical clearance.
*   **DON'T** use the Lime Green for large background areas; it is a high-energy accent for buttons and selection chips only.