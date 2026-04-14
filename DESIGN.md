# Design System Strategy: Architectural Precision & Local Authority

## 1. Overview & Creative North Star
This design system is built upon the Creative North Star of **"The Master Craftsman’s Portfolio."** Unlike standard "service provider" websites that rely on cluttered grids and loud sales banners, this system adopts a high-end editorial approach. It treats every fence post and railing assembly as a piece of architectural art. 

The aesthetic marries the industrial strength of charcoal and slate with the refined, spacious layouts found in luxury architectural journals. We break the "template" look through **intentional asymmetry**: utilizing oversized typography that bleeds off-center, overlapping imagery that breaks container boundaries, and a sophisticated layering of monochromatic surfaces that creates depth without the need for dated drop shadows.

## 2. Colors
The palette is rooted in permanence and structural integrity. It leverages deep slates and charcols to provide a "blue-collar luxury" foundation.

| Token | Hex | Role |
| :--- | :--- | :--- |
| `primary` | `#05152b` | Deep Navy: Use for authoritative headings and core branding. |
| `secondary` | `#a73918` | Construction Rust: High-action CTAs and craftsmanship highlights. |
| `surface` | `#f9f9fb` | The Canvas: Provides a clean, modern architectural backdrop. |
| `surface-container` | `#edeef0` | Structural Mid-tone: Used for subtle sectioning. |
| `tertiary` | `#04171f` | Slate Charcoal: Accents and deep contextual backgrounds. |

### The "No-Line" Rule
To maintain a premium, custom feel, **1px solid borders are prohibited for sectioning.** Boundaries must be defined solely through background color shifts. For example, a content block using `surface-container-low` should sit directly against a `surface` background. This creates a "molded" look rather than a "boxed" look.

### Surface Hierarchy & Nesting
Treat the UI as a physical assembly. Use `surface-container-lowest` for the primary background and "nest" interactive elements within higher tiers like `surface-container-high` to create natural prominence.

### Signature Textures & Glass
Main CTAs should utilize a subtle linear gradient transitioning from `primary` to `primary-container`. For floating navigation or mobile menus, apply **Glassmorphism**: use `surface` at 80% opacity with a `24px` backdrop-blur to allow project photography to bleed through the UI, softening the interface.

## 3. Typography
The typographic system uses a high-contrast pairing to balance technical precision with approachable craftsmanship.

*   **Display & Headlines (`Space Grotesk`):** A geometric sans-serif with idiosyncratic "industrial" details. Used for high-impact statements. The tight tracking and oversized scale communicate modern authority.
*   **Body & Titles (`Manrope`):** A highly readable, functional typeface that bridges the gap between tech-forward and human-centric. Use `body-lg` for project descriptions to ensure an editorial feel.
*   **Labels (`Work Sans`):** Optimized for utility. Used for technical specs, dimensions, and small-scale metadata.

## 4. Elevation & Depth
In this system, depth is a result of **Tonal Layering**, not structural decoration.

*   **The Layering Principle:** Stacking tiers (e.g., a `surface-container-lowest` card on a `surface-container-low` section) creates a soft, architectural lift. This mimics how materials like wood and steel overlap in real-world construction.
*   **Ambient Shadows:** If a floating effect is required (e.g., a "Get a Quote" modal), use a tinted shadow: `0px 24px 48px rgba(5, 21, 43, 0.06)`. This uses the `primary` color to simulate natural ambient light.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use the `outline-variant` token at **15% opacity**. It should be felt, not seen.
*   **Glassmorphism:** Reserved for top-tier interactions. Use semi-transparent `surface` colors to create "frosted" overlays that integrate the UI with high-resolution imagery of the physical builds.

## 5. Components

### Buttons: The "Solid Lead" Style
*   **Primary:** `secondary` background, `on-secondary` text. No border. `md` (0.375rem) roundedness.
*   **Secondary:** `primary` background with a 10% `surface-tint` overlay on hover. 
*   **Tertiary:** Transparent background, `primary` text, with an underline that expands from the center on hover.

### Cards: The "Seamless" Gallery
*   **Style:** Forbid the use of divider lines. Separate content using vertical white space and font weight shifts.
*   **Interaction:** On hover, a card should shift from `surface-container-low` to `surface-container-highest` with a subtle `2px` upward translation.

### Input Fields: The "Blueprint" Style
*   **Style:** No background fill. Use a "Ghost Border" (15% `outline-variant`) on three sides, with a thicker `2px` `primary` bottom border to ground the input.
*   **Focus:** Transition the bottom border to `secondary` to signal active "construction" mode.

### Signature Component: The "Craftsmanship Loupe"
A specialized image component for gallery pages. A large-scale project photo that, upon hover, reveals a high-detail "loupe" or zoomed-in window showing the precision of the welds, wood grain, or cable tension.

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts where text blocks overlap image edges by 20-40px.
*   **Do** prioritize high-resolution "action" photography (e.g., close-ups of stainless steel fittings or treated wood textures).
*   **Do** use `display-lg` typography for short, punchy value propositions (e.g., "Built Once. Built Right.").

### Don't:
*   **Don't** use standard "Construction Orange." Stick to the sophisticated `secondary` (#a73918) for a more premium, weathered feel.
*   **Don't** use 100% black text. Use `on-surface` (#1a1c1e) to keep the contrast high but the feel sophisticated.
*   **Don't** use generic icons. Use thin-stroke, custom SVG icons that mimic architectural blueprints or technical drawings.