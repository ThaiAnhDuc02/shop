# Design System Document: The Editorial Alchemist

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Digital Atelier."** We are not building a standard e-commerce interface; we are curating a sensory experience that mirrors the tactility of a luxury perfume house. 

To achieve this, the system moves away from the "boxed" nature of the web. We embrace **Intentional Asymmetry**—where imagery and typography overlap to create depth—and **Breathtaking Negative Space**. The goal is to make the user feel as though they are flipping through a high-end, limited-edition fashion monograph. Every element must feel "placed" rather than "potted," favoring an editorial layout over a rigid functional grid.

---

## 2. Colors: The Palette of Scent
The color strategy avoids the harshness of digital "pure" colors, favoring an organic, weighted palette that feels expensive.

### Color Tokens
*   **Primary (#755a26):** "Aged Gold." Used for moments of prestige and brand authority.
*   **Background (#fdf9f4):** "Soft Cream." A warm, breathable base that replaces clinical white.
*   **On-Surface (#1c1c19):** "Deep Velvet Black." High-contrast legibility for copy.
*   **Surface Tiers:** Use `surface-container-low` (#f7f3ee) for large sectioning and `surface-container-highest` (#e6e2dd) for subtle callouts.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders for sectioning or containment. Boundaries must be defined solely through background color shifts. For instance, a product detail section in `surface-container-low` should sit directly against a `surface` background. The transition is the border.

### The "Glass & Gradient" Rule
To add "soul," use subtle gradients. Instead of a flat gold button, use a linear gradient from `primary` (#755a26) to `primary-container` (#af8f55). For floating navigation or modals, apply **Glassmorphism**: use `surface` at 80% opacity with a `24px` backdrop-blur to allow the rich perfume photography to bleed through the UI.

---

## 3. Typography: The Voicing of Elegance
Typography is our primary tool for conveying luxury. We pair the authoritative weight of a serif with the invisible precision of a sans-serif.

*   **Display & Headlines (Noto Serif):** These are the "Hero" elements. Use `display-lg` (3.5rem) with tight letter-spacing for a dramatic editorial impact. Headlines should often be center-aligned or dramatically offset to break the vertical rhythm.
*   **Body & Labels (Manrope):** Chosen for its clean, architectural lines. Use `body-md` (0.875rem) for most descriptions. For luxury appeal, increase the line-height (leading) to 1.6 to ensure the text "breathes."
*   **Visual Hierarchy:** High contrast in scale is mandatory. A `display-lg` headline should sit near a `label-md` sub-header to create a "Couture" typographic tension.

---

## 4. Elevation & Depth: Tonal Layering
Traditional dropshadows are too "digital" for this brand. We create depth through physical stacking concepts.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` section. This creates a "Paper-on-Paper" effect.
*   **Ambient Shadows:** If a floating element (like a shopping bag) requires a shadow, it must be invisible to the untrained eye. Use the `on-surface` color at 4% opacity with a `48px` blur and `12px` Y-offset.
*   **The "Ghost Border" Fallback:** Only if accessibility requires it, use `outline-variant` (#d1c5b5) at **15% opacity**. Anything more is a design failure.
*   **Glassmorphism:** Use semi-transparent layers for any UI that sits over photography. This ensures the "Scent" (the image) is always present behind the "Structure" (the UI).

---

## 5. Components: Editorial Elements

### Buttons
*   **Primary:** Rectangular with a `0.25rem` (sm) radius. Background: `primary` gradient. Text: `on-primary` in `label-md` (all caps, 0.1em letter spacing).
*   **Secondary:** No background. A "Ghost Border" (15% opacity) and `primary` text.
*   **Interaction:** On hover, the primary button should subtly shift in tonal depth rather than changing color entirely.

### Cards & Lists
*   **Forbid Dividers:** Horizontal lines are banned. Use `spacing-12` (4rem) to separate list items or shift the background color slightly.
*   **Product Cards:** Use asymmetrical padding. An image might bleed to the top and left, while text is tucked into the bottom right with significant white space.

### Input Fields
*   **Style:** Minimalist underline only, using `outline` (#7f7668) at 30% opacity. 
*   **State:** On focus, the underline transitions to `primary` gold. Helper text must be in `label-sm` and feel like a footnote in a magazine.

### Signature Component: The "Scent Fragment" (Chip)
*   Used for notes (e.g., Oud, Bergamot). These should be `surface-container-highest` with a `full` (9999px) radius and `body-sm` text. They should feel like smooth river stones.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** allow images to break the container. An elegant perfume bottle should overlap the section below it.
*   **Do** use extreme white space. If you think there is enough space, add 20% more.
*   **Do** treat "Add to Cart" as a moment of ceremony, not just a utility.

### Don’t:
*   **Don’t** use "pure" black (#000000) or "pure" white (#FFFFFF). Use the Velvet Black and Soft Cream tokens.
*   **Don’t** use standard icons. Use thin-stroke (1pt or 0.5pt) custom iconography that matches the weight of the sans-serif text.
*   **Don’t** center-align everything. Use the 12-column grid to "anchor" elements at different start points to create an asymmetrical, professional feel.

---

## 7. Spacing Scale
*   **Micro (Spacing 1-3):** For internal component padding.
*   **Macro (Spacing 16-24):** For vertical sectioning. We favor large gaps (`5.5rem` to `8.5rem`) to ensure the user’s eye rests between content "chapters."