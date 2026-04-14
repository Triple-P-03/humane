# Design System Documentation: The Editorial Philanthropist

## 1. Overview & Creative North Star
### Creative North Star: "The Modern Curator"
This design system rejects the "template-heavy" look of traditional non-profits. Instead, it adopts the persona of a high-end digital gallery. The goal is to elevate NGO work from "charity" to "prestige." We achieve this through **Editorial Authority**: using extreme scale in typography, intentional asymmetry that guides the eye, and a "less is more" philosophy regarding UI chrome. 

The experience should feel like a premium tech-forward publication—think *Kinfolk* meets *Stripe*. We do not use boxes to contain ideas; we use space to let them breathe.

---

## 2. Colors & Surface Philosophy
The palette is a sophisticated interplay between deep Charcoals (`secondary`), Crisp Whites (`surface`), and a singular, high-energy "Impact Yellow" (`primary_container`).

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to section content. Boundaries must be defined through:
*   **Color Shifts:** Transitioning from `surface` to `surface_container_low`.
*   **Tonal Transitions:** Using `surface_container_high` for inset modules.
*   **Negative Space:** Using at least `spacing-16` (5.5rem) between major thematic blocks to signal a transition.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine paper. 
1.  **Base Layer:** `surface` (#fcf9f8) – The canvas.
2.  **Section Layer:** `surface_container_low` (#f6f3f2) – To group related content blocks.
3.  **Component Layer:** `surface_container_lowest` (#ffffff) – Used for cards or interactive modules to make them "pop" against the canvas.

### The "Glass & Gradient" Rule
To avoid a flat, "Bootstrap" feel:
*   **Glassmorphism:** For navigation bars or floating action panels, use `surface` at 80% opacity with a `24px` backdrop blur.
*   **Signature Textures:** For high-conversion CTAs, use a subtle linear gradient from `primary` (#705d00) to `primary_container` (#FFD700) at a 135-degree angle. This adds "soul" and a metallic, premium sheen to the accent yellow.

---

## 3. Typography: Plus Jakarta Sans
We use **Plus Jakarta Sans** for its geometric clarity and modern humanist terminals. It provides the "tech-non-profit" edge required.

*   **Display (Display-LG/MD):** Used for "Statement Headlines." Use `on_surface` (#1c1b1b) with a letter-spacing of `-0.02em`. These should often be paired with high-quality imagery in an asymmetrical layout.
*   **Headlines (Headline-LG):** The workhorse for section titles. Keep these tight and authoritative.
*   **Body (Body-LG):** Optimized for readability. Use `secondary` (#5f5e5e) to reduce optical vibrating against the crisp white background, ensuring a comfortable editorial long-read.
*   **Labels (Label-MD):** Always uppercase with `+0.05em` tracking when used for categorization or eyebrow heads above titles.

---

## 4. Elevation & Depth
We eschew traditional shadows in favor of **Tonal Layering**. 

*   **The Layering Principle:** Place a `surface_container_lowest` card on a `surface_container_low` section. The slight delta in hex value creates a "natural lift" that feels architectural rather than digital.
*   **Ambient Shadows:** If a floating element (like a modal or dropdown) is required, use a custom shadow:
    *   `Y: 20px, Blur: 40px, Color: rgba(28, 27, 27, 0.06)` (A tint of `on_surface`).
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke (e.g., in high-contrast modes), use `outline_variant` at **15% opacity**. Never use a 100% opaque border.

---

## 5. Components

### Buttons
*   **Primary:** `primary_container` (#FFD700) background with `on_primary_container` text. 12px (`md`) corner radius. High-gloss hover state using the signature gradient.
*   **Tertiary (Editorial Link):** No background. `on_surface` text with a 2px underline in `primary` that sits 4px below the baseline.

### Cards & Lists
*   **The Divider Ban:** Never use horizontal rules `<hr>`. Separate list items using `spacing-4` (1.4rem) and a background shift on hover to `surface_container_high`.
*   **Image Containers:** Images must always use the `md` (12px) or `lg` (1rem) roundness to soften the "tech" edge and make the brand feel approachable.

### Input Fields
*   **Styling:** Use `surface_container_highest` as the fill. No border. On focus, transition the background to `surface` and add a 2px "Ghost Border" using the `primary` color.

### Signature Component: The "Impact Stat"
A large `display-lg` number in `on_surface` paired with a `label-md` description in `primary`. These should be placed asymmetrically on the grid, breaking the vertical flow of text to grab attention.

---

## 6. Do's and Don'ts

### Do
*   **Do** use "Full-Bleed" imagery that goes behind the navigation bar for a cinematic feel.
*   **Do** use the `spacing-24` (8.5rem) token for bottom margins on Hero sections.
*   **Do** lean into the "Impact Yellow" sparingly—it is a spotlight, not a floodlight.

### Don't
*   **Don't** use pure black (#000000). Use the Charcoal (`on_surface` #1c1b1b) to maintain the editorial softness.
*   **Don't** use standard 8px rounding. Stick strictly to the **12px (md)** or **16px (lg)** scale to maintain the "Modern Tech" look.
*   **Don't** center-align long blocks of text. Editorial layouts are traditionally left-aligned or use "Negative Space Pull-Quotes" to the right.

### Accessibility Note
While we favor subtle tonal shifts, always ensure that text-to-background contrast ratios meet WCAG AA standards. When using the `primary_container` yellow, ensure the text color is `on_primary_container` (#705e00) to maintain legibility.