# Design System Strategy: The Analytical Editorial

## 1. Overview & Creative North Star
**Creative North Star: The Sovereign Scholar**
This design system moves beyond the "template" look of a standard CV. It is a digital manifestation of precision, academic rigor, and financial sophistication. Instead of a rigid, boxed-in layout, we employ an editorial approach—treating the screen like a high-end financial journal. 

The aesthetic is driven by **Intentional Asymmetry**. We break the expected grid by using expansive "white space" (utilizing `surface`) contrasted with dense, structured data clusters. By overlapping serif display typography with minimalist sans-serif data points, we create a signature visual identity that feels both established and modern. This is not a website; it is a curated portfolio of intellectual capital.

---

## 2. Colors & Surface Architecture
The palette is rooted in deep, authoritative tones. We avoid pure blacks and whites to maintain a "printed" feel.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections. Structural boundaries must be achieved through:
- **Background Color Shifts:** Use `surface_container_low` for a main section and `surface_container` for an inset data area.
- **Tonal Transitions:** Define depth by placing a `surface_container_lowest` card on a `surface` background.

### Surface Hierarchy & Nesting
Treat the UI as a series of layered, high-quality paper stocks. 
- **Base Layer:** `surface` (#fbf8ff)
- **Content Blocks:** `surface_container_low` (#f4f2ff)
- **Elevated Data Points:** `surface_container_highest` (#e0e0fc)

### The "Glass & Gradient" Rule
To evoke the high-end feel of modern fintech, use **Glassmorphism** for floating elements (like a navigation bar or a sticky action menu). Use `surface_variant` at 60% opacity with a `backdrop-blur` of 20px. 

### Signature Textures
For Hero backgrounds or primary CTAs, do not use flat colors. Use a subtle linear gradient from `primary_container` (#101b30) to `secondary` (#47607e) at a 135-degree angle. This adds "soul" and prevents the design from feeling sterile.

---

## 3. Typography
The typography system is a dialogue between two eras: the classic academic serif and the modern, data-driven sans-serif.

*   **Headlines (Newsreader):** The Serif choice. Use `display-lg` through `headline-sm` for all major headings. This conveys institutional authority and "academic rigor." Ensure tight letter-spacing (-0.02em) for large display sizes to maintain a premium feel.
*   **Body & Data (Manrope):** The Sans-Serif choice. Use `body-lg` for narrative and `label-md` for data-heavy sections. Manrope’s geometric clarity suggests an analytical, modern mind.
*   **Hierarchy Note:** Use `tertiary` (#735c00) sparingly for `label-sm` elements to highlight key metrics or "Gold Standard" achievements.

---

## 4. Elevation & Depth
We eschew traditional "Drop Shadows" in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by "stacking." A card using `surface_container_lowest` sitting on `surface` provides a "natural lift" that feels architectural rather than digital.
*   **Ambient Shadows:** If a floating state is required (e.g., a modal or a primary button hover), use a shadow with a 32px blur, 0px offset, and 6% opacity using the `on_surface` color. It should feel like a soft glow, not a hard edge.
*   **The "Ghost Border" Fallback:** If accessibility requires a container edge, use `outline_variant` (#c4c6cc) at **15% opacity**. High-contrast borders are strictly forbidden as they clutter the analytical clarity.

---

## 5. Components

### Buttons
*   **Primary:** Background: `primary` (#000000) or a gradient of `primary_container` to `secondary`. Text: `on_primary`. Radius: `md` (0.375rem).
*   **Secondary:** Background: `secondary_container`. Text: `on_secondary_container`. No border.
*   **Tertiary (The "Academic Link"):** No background. Use `Newsreader` (serif) in `secondary` with a 1px underline using `outline_variant`.

### Cards & Lists (CV Sections)
*   **Rule:** Forbid divider lines between list items. 
*   **Execution:** Use `spacing-6` (1.5rem) to separate experience items. Use a subtle background shift (`surface_container_low`) on hover to indicate interactivity.
*   **Data Tables:** For mathematical proofs or financial models, use `surface_container_highest` for the header row and `surface` for the body. Use `label-md` (Manrope) for all numerical data to ensure alignment.

### Chips (Skills & Tags)
*   Use `surface_container_high` with `label-sm` text. 
*   Corner radius: `full` (9999px) for a modern, pill-shaped look that contrasts with the sharper `md` corners of the cards.

### Interactive CV Timeline
*   Instead of a line, use a vertical progression of `secondary_fixed` (#d1e4ff) dots. This suggests a "plotted" data path, echoing the mathematics theme.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Margin:** Use `spacing-24` (6rem) for page gutters. The more "room to breathe," the more premium the portfolio feels.
*   **Align to a Baseline:** Ensure all typography sits on a consistent vertical rhythm. Precision is a brand value.
*   **Use Mono-spaced Numbers:** If possible, use the tabular-nums feature of Manrope for financial data so decimals align perfectly.

### Don’t:
*   **Don't use pure blue:** The palette uses `secondary` (#47607e) which is a muted, sophisticated slate-blue. Avoid "standard" hyperlink blue at all costs.
*   **Don't use heavy rounding:** Avoid `xl` or `2xl` corner radii. Keep it to `sm` or `md` to maintain a professional, sharp-edged academic feel.
*   **Don't overcrowd:** If a section feels full, increase the `spacing` token rather than shrinking the text.