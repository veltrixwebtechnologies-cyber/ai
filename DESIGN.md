```markdown
# Design System Specification

## 1. Overview & Creative North Star: "The Digital Jurist"
This design system is built upon the concept of **The Digital Jurist**. It rejects the cluttered, "dashboard-heavy" tropes of modern SaaS in favor of an elite, editorial experience that mirrors the precision of a legal audit and the speed of artificial intelligence.

The visual signature is defined by **Absolute Flatness** and **Architectural Geometry**. By removing all shadows, gradients, and rounded corners (0px radius), we create a high-stakes environment where the data is the hero. The aesthetic is "Technical Brutalism" met with "High-Fashion Minimalism"—it is intentional, uncompromising, and lightweight. We break the template look by utilizing radical whitespace and a strict adherence to a monochromatic foundation, punctuated only by functional status colors.

---

## 2. Colors & Tonal Logic
The palette is rooted in absolute contrast. We use `primary` (#000000) against a `surface` (#f9f9f9) to establish authority.

### The "No-Line" Rule
To maintain a premium feel, 1px solid borders are strictly prohibited for sectioning. Structural boundaries must be defined through **Background Shifts**. 
*   **Hierarchy via Tone:** Use `surface_container_low` (#f3f3f3) to define a sidebar and `surface` (#f9f9f9) for the main stage. 
*   **Nesting:** To create focus without shadows, nest a `surface_container_lowest` (#ffffff) card within a `surface_container` (#eeeeee) wrapper. This "paper-on-paper" layering creates a sophisticated depth that feels physical rather than digital.

### Functional Palette
Status is the only reason to break the monochrome rule.
*   **Critical (Red):** `error` (#ba1a1a) – Use for failed audits or severe vulnerabilities.
*   **Warning (Amber):** Use `secondary_fixed` (#c8c6c6) logic but mapped to a high-contrast Amber for functional alerts.
*   **Good (Green):** Mapped to high-contrast functional Green for passed audits.

### Signature Textures
While the system is "flat," we achieve "visual soul" by using `outline_variant` (#c6c6c6) at 20% opacity for "Ghost Borders" only when absolutely necessary for accessibility in input fields. Otherwise, let the edges of the color blocks define the space.

---

## 3. Typography: The Editorial Voice
We use a dual-typeface system to distinguish between the "Judge" (The UI) and the "Evidence" (The Code).

*   **Display & Headlines (Manrope):** The variable sans-serif `manrope` provides a modern, professional weight. Large `display-lg` (3.5rem) should be used with generous leading to create an editorial feel in report summaries.
*   **UI & Body (Inter):** `inter` provides maximum legibility at small sizes. All UI labels and body copy must use **Sentence case** to feel approachable and modern. Avoid ALL CAPS as it feels like "shouting" in an audit context.
*   **The Evidence (Monospace):** Use a small monospaced font (mapped to `label-sm`) for code snippets, URLs, and raw data strings. This creates a clear visual distinction between the AI's "opinion" (Sans) and the "facts" (Mono).

---

## 4. Elevation & Depth: Tonal Layering
Traditional elevation (Z-index) is conveyed through **Tonal Stacking** rather than light and shadow.

*   **The Layering Principle:** 
    1. Base Level: `surface` (#f9f9f9)
    2. Interactive/Lowered Level: `surface_container_low` (#f3f3f3)
    3. Elevated/Focus Level: `surface_container_lowest` (#ffffff)
*   **Zero Shadows:** Shadow tokens are deprecated. If an element needs to "float" (like a modal), use a high-contrast `outline` (#777777) at 1px width.
*   **Flat Glassmorphism:** For overlays, use a semi-transparent `surface` color with a `backdrop-filter: blur(10px)`. This keeps the "Lightweight" promise while allowing the underlying audit data to remain visible, softening the UI’s geometry.

---

## 5. Components

### Buttons
Buttons are strictly rectangular (0px radius).
*   **Primary:** `primary` (#000000) background with `on_primary` (#e2e2e2) text. No hover shadow; use a 90% opacity shift on hover.
*   **Secondary:** `outline` border (1px) with no background.
*   **Tertiary:** Text-only, using `primary` with a underline that appears only on hover.

### Input Fields
*   **Style:** `surface_container_lowest` background with a 1px `outline_variant` border.
*   **Focus:** Border shifts to `primary` (#000000). No "glow" or shadow.
*   **Labels:** Always `label-md` in `on_surface_variant` (#474747), positioned above the field.

### Audit Result Cards
*   **Prohibition:** No divider lines.
*   **Layout:** Use `spacing-6` (2rem) between cards. Differentiate categories of audits using a 4px left-accent bar in the functional color (Red/Amber/Green).
*   **Background:** Use `surface_container_low` for the card body to distinguish it from the `surface` background.

### Status Chips
*   **Geometry:** Rectangular.
*   **Coloring:** High-contrast background (e.g., `error_container`) with high-contrast text (`on_error_container`).

---

## 6. Do’s and Don’ts

### Do
*   **Do** use `spacing-16` and `spacing-20` to separate major sections. The "Generous Whitespace" is the UI's most expensive-looking feature.
*   **Do** use **Sentence case** for everything, including headers. "Audit report summary" is correct; "Audit Report Summary" is incorrect.
*   **Do** ensure all interactive elements have a distinct `hover` state using tonal shifts (e.g., from `surface_container` to `surface_container_high`).

### Don't
*   **Don't** use a border-radius of any kind. This system is 0px by design.
*   **Don't** use icons as a primary navigation source. Pair them with `label-md` text to maintain an authoritative, professional tone.
*   **Don't** use 1px dividers to separate list items. Use `spacing-4` padding and `surface` shifts instead.
*   **Don't** use blue for links. Links are `primary` (#000000) with a subtle underline to maintain the high-contrast aesthetic.```