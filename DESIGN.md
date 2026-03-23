# Design System Strategy: The Curated Intelligence

## 1. Overview & Creative North Star: "The Digital Curator"
This design system rejects the frantic, "noisy" aesthetic of typical AI startups. Our Creative North Star is **The Digital Curator**. We treat information as a high-end gallery space—expensive, quiet, and intentional. 

To move beyond "template" UI, we utilize **Intentional Asymmetry**. Instead of a rigid, centered grid, we lean into generous left-aligned typography contrasted against expansive white space. We break the "box" mentality by allowing high-end imagery and typography to overlap across tonal surface shifts, creating a sense of depth that feels architectural rather than digital.

## 2. Colors & Surface Philosophy
The palette is rooted in organic, warmth-leaning neutrals to establish immediate trust.

### Surface Hierarchy & Nesting
We do not use borders to define space. We use **Tonal Nesting**.
- **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Boundaries are created through background shifts.
- **Base Layer:** Use `surface` (#fbf9f4) for the main page canvas.
- **In-Page Sections:** Use `surface-container-low` (#f5f4ed) to define distinct content blocks.
- **Elevated Components:** Place `surface-container-lowest` (#ffffff) cards atop a `surface-container-low` background to create a "lifted paper" effect.

### The Glass & Gradient Rule
To ensure the "premium" feel isn't "flat," use Glassmorphism for floating navigation and overlays.
- **Token:** `surface` at 80% opacity with a `24px` backdrop-blur.
- **Signature Textures:** For primary CTAs, use a subtle linear gradient from `primary` (#5f5e5e) to `primary-dim` (#535252) at a 145-degree angle. This adds a "weighted" feel that flat hex codes cannot achieve.

## 3. Typography: The Editorial Voice
We use a high-contrast pairing of **Manrope** for authority and **Inter** for utility.

*   **Display & Headlines (Manrope):** These are our "Editorial" levels. Use `display-lg` (3.5rem) with a negative letter-spacing of `-0.02em` to create a dense, authoritative "masthead" look.
*   **Body & Labels (Inter):** These are our "Functional" levels. Use `body-lg` (1rem) with a generous line-height (1.6) and `0.01em` letter-spacing to ensure the "spacious" feel requested by the firm.
*   **Hierarchy Tip:** Always skip a size in the scale when transitioning from a headline to body text (e.g., `headline-lg` directly to `body-lg`) to create a dramatic, high-end contrast.

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "tech." We use **Ambient Occlusion** logic.

- **The Layering Principle:** Depth is achieved by stacking. A `surface-container-highest` (#e2e3d9) element should only exist inside a `surface-container` (#efeee6) wrapper.
- **Ambient Shadows:** For floating elements, use a multi-layered shadow:
  - `0px 4px 20px rgba(49, 51, 44, 0.04)`
  - `0px 12px 40px rgba(49, 51, 44, 0.06)`
- **The "Ghost Border":** If accessibility requires a stroke, use `outline-variant` (#b1b3a9) at **15% opacity**. It should be felt, not seen.

## 5. Components

### Buttons & Interaction
- **Primary:** `primary` (#5f5e5e) background with `on-primary` (#faf7f6) text. Shape: `Roundedness.md` (0.375rem).
- **Secondary (The Muted Gold):** Use `tertiary` (#785a1a) text with no background, only an underline on hover. This maintains the "minimalist" aesthetic.
- **Tertiary/Ghost:** Use `secondary-fixed-dim` (#cbd5e8) for low-priority actions like "Cancel."

### Input Fields & Forms
- **Resting State:** `surface-container-highest` background, no border.
- **Focus State:** A 1px `outline` (#797c73) transition with a subtle 4px "glow" using the `tertiary` color at 10% opacity.
- **Labels:** Use `label-md` in `on-surface-variant` (#5e6058), positioned 0.5rem above the input.

### Cards & Lists
- **Forbid Dividers:** Never use horizontal lines. Use `Spacing.6` (2rem) of vertical white space to separate list items.
- **The "Insight" Card:** A `surface-container-lowest` card with `Roundedness.lg` (0.5rem). The header should use `tertiary` (#785a1a) for small accents to denote "AI Intelligence."

### Navigation Bar
- **Style:** A "Floating Island" design. Instead of a full-width bar, use a centered container with `9999px` (full) roundedness, using the Glassmorphism rule defined in Section 2.

## 6. Do's and Don'ts

### Do:
- **Use "Extreme" White Space:** If you think there is enough space, add `Spacing.4` more. 
- **Layer Tones:** Use `surface-container-low` to group related content instead of drawing a box around it.
- **Optical Kerning:** Manually tighten headings that start with "W", "V", or "T" to maintain the premium editorial feel.

### Don't:
- **Don't use 100% Black:** Always use `on-background` (#31332c) for text to keep the "Cream/Charcoal" sophisticated warmth.
- **Don't use Grids for Everything:** Allow some elements (like pull-quotes or decorative AI icons) to sit "off-grid" to break the digital rigidity.
- **Don't use Hover Shadows:** Instead of a shadow on hover, shift the background color from `surface` to `surface-container-low`. It feels more architectural and less "clickable."