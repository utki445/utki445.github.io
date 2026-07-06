---
name: Arcade Noir
colors:
  surface: '#131318'
  surface-dim: '#131318'
  surface-bright: '#39383e'
  surface-container-lowest: '#0e0e13'
  surface-container-low: '#1b1b20'
  surface-container: '#1f1f25'
  surface-container-high: '#2a292f'
  surface-container-highest: '#35343a'
  on-surface: '#e4e1e9'
  on-surface-variant: '#b9cacb'
  inverse-surface: '#e4e1e9'
  inverse-on-surface: '#303036'
  outline: '#849495'
  outline-variant: '#3a494b'
  surface-tint: '#00dbe7'
  primary: '#e1fdff'
  on-primary: '#00363a'
  primary-container: '#00f2ff'
  on-primary-container: '#006a71'
  inverse-primary: '#00696f'
  secondary: '#e9b3ff'
  on-secondary: '#510074'
  secondary-container: '#7d01b1'
  on-secondary-container: '#e5a9ff'
  tertiary: '#fff6e4'
  on-tertiary: '#3a3000'
  tertiary-container: '#ffd81d'
  on-tertiary-container: '#715e00'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#74f5ff'
  primary-fixed-dim: '#00dbe7'
  on-primary-fixed: '#002022'
  on-primary-fixed-variant: '#004f54'
  secondary-fixed: '#f6d9ff'
  secondary-fixed-dim: '#e9b3ff'
  on-secondary-fixed: '#310048'
  on-secondary-fixed-variant: '#7200a3'
  tertiary-fixed: '#ffe16d'
  tertiary-fixed-dim: '#e9c400'
  on-tertiary-fixed: '#221b00'
  on-tertiary-fixed-variant: '#544600'
  background: '#131318'
  on-background: '#e4e1e9'
  surface-variant: '#35343a'
typography:
  h1:
    fontFamily: Inter
    fontSize: 48px
    fontWeight: '800'
    lineHeight: '1.1'
    letterSpacing: -0.04em
  h2:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  h3:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
    letterSpacing: -0.01em
  body-base:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
    letterSpacing: '0'
  code-sm:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '400'
    lineHeight: '1.5'
    letterSpacing: '0'
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '700'
    lineHeight: '1'
    letterSpacing: 0.1em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 4px
  gutter: 24px
  margin: 48px
  container-max: 1200px
  dot-path-gap: 16px
---

## Brand & Style

This design system establishes a "Premium Technical Play" aesthetic. It merges the structured, documentation-first rigor of a GitHub profile with the high-energy, nostalgic pulse of a retro arcade. The brand personality is that of a "Master Craftsperson who hasn't forgotten how to play"—balancing high-end engineering credibility with creative whimsy.

The visual style is a hybrid of **Glassmorphism** and **Minimalism**, utilizing translucent layers to suggest depth and modern sophistication. This is punctuated by "8-bit high-fidelity" accents: sharp, pixel-inspired geometry executed with modern gradients and soft blurs. The emotional goal is to evoke curiosity, nostalgia, and a sense of technical excellence.

## Colors

The palette utilizes a "Neon-on-Ink" strategy for the default Dark Mode. The primary **Neon Cyan** represents Pacman’s classic environment energy, while the **Purple** secondary adds a premium, modern depth. **Tertiary Gold** is reserved strictly for Pacman-specific motifs (the "hero" element and power pellets).

In Light Mode, the intensity is dialed back into soft pastels to maintain readability while preserving the chromatic relationship. Gradients should be used sparingly, primarily for high-level interactive states and progress paths.

## Typography

Typography follows a functional hierarchy inspired by developer documentation. **Inter** provides a neutral, high-legibility foundation for all prose and headings, ensuring the portfolio feels professional and accessible.

**JetBrains Mono** is the "voice of the machine." Use it for technical metadata, snippets, and navigation labels. This font pairing mirrors the GitHub README aesthetic, signaling technical proficiency. Headings should use tighter letter spacing to feel "heavy" and authoritative, contrasting against the airy, monospaced tech labels.

## Layout & Spacing

The layout employs a **fixed-width container grid** (12-column) centered on the screen, mimicking the structured feel of a GitHub profile page. Components are modular, "bento-box" style tiles that snap to the grid.

A unique "Dot Path" spacing rhythm is used for vertical transitions. Instead of standard dividers, use a sequence of small circular "pellets" spaced at 16px intervals to guide the eye between sections. Content should be grouped into logical "Modules" with consistent padding to maintain the organized, documentation-heavy feel.

## Elevation & Depth

This design system rejects traditional drop shadows in favor of **Glassmorphic stacking** and **inner glows**.

1.  **Base Layer:** The solid background (#0a0a0f).
2.  **Surface Layer:** Semi-transparent cards with a `backdrop-filter: blur(12px)`.
3.  **Ghost Elevation:** Instead of shadows, use a 1px solid border with 10% opacity white. On hover, this border transitions to a neon gradient to simulate "powering up."
4.  **Z-Index Depth:** Interaction with "Ghost" elements (the maze antagonists) should trigger a slight "lift" effect using a soft outer glow in the ghost's specific color (Red, Pink, Cyan, Orange).

## Shapes

The shape language is primarily **Soft (0.25rem)** to maintain a disciplined, "coded" appearance. While the "Pacman" and "Pellet" motifs are perfectly circular, the UI containers themselves remain subtly rounded rectangles. This tension between the round character elements and the sharp UI containers reinforces the "Professional vs. Playful" brand split.

Avoid fully pill-shaped buttons; instead, use the `rounded-lg` (0.5rem) setting for interactive elements to make them feel more tactile and "clickable" than the static layout blocks.

## Components

### Buttons & Inputs
Buttons should feel like arcade console triggers. Use a subtle inner-bevel gradient in the primary color. Monospace labels only.
*   **Default:** Glass background with thin border.
*   **Primary:** Solid gradient background with black text for high contrast.

### Cards (The "README" Modules)
Cards are the primary container. They must include a "Header" strip (like a terminal window or a GitHub card header) with a monospace title and a subtle icon.

### Pacman Accents
*   **The Loader:** A Pacman silhouette eating a trail of 3 dots.
*   **The Path:** Use dotted borders for inactive states and solid neon lines for active "high-score" states.
*   **Ghost Chips:** For skill tags, use small "Ghost" icons (Blinky, Pinky, etc.) next to the technology name.

### Progress Bars
Progress bars should be stylized as "Level Maps." A Pacman icon sits at the current percentage point, with "consumed" dots behind it and "active" dots ahead of it.