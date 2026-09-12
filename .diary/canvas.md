## 2023-10-24 - Canvas Visual System & Token Architecture

**Learning:** The legacy chat interface relied on hardcoded hex values and element style overrides for theme switching (`body.style.backgroundColor`). This caused major theme parity bugs where input components and message containers remained dark gray when switching to light mode. Using `data-theme="light|dark"` at the root document level tied to CSS custom properties ensures 100% theme coverage and component consistency across light and dark modes.

**Action:** Standardized all UI surfaces using tokenized CSS custom variables (`--bg-app`, `--bg-surface`, `--bg-user-msg`, `--bg-bot-msg`, `--bg-input-box`, `--border-subtle`, `--border-focus`, `--accent-primary`). Configured focus-visible indicators (`:focus-visible`) and animated thinking state indicators (`.typing-indicator`) for seamless state communication.

## 2025-03-09 - Design Token Refinement & Motion Standards

**Learning:** Replacing hardcoded hex values (such as `#ffffff` on primary button states, brand icons, and message avatars) with tokenized variables (`--text-on-accent`) eliminates contrast inconsistencies when themes or accent colors are customized. Standardizing avatar sizing via `--avatar-size` and adding `@media (prefers-reduced-motion: reduce)` ensures consistent visual component dimensions and user accessibility preferences across all states.

**Action:** Defined `--text-on-accent` and `--avatar-size` tokens in `:root`, standardized component focus rings (`:focus-visible`), updated all hardcoded `#ffffff` foreground styles to use design tokens, and implemented prefers-reduced-motion CSS support.

## 2025-03-09 - Vector SVG Icon Replacement

**Learning:** System emojis (e.g. 🤖, 🌙, ☀️, 💬) render inconsistently across operating systems and platforms, leading to alignment, sizing, and color tinting discrepancies in design systems. Using inline SVG vector graphics with `fill: currentColor` ensures seamless color inheritance from design tokens, predictable scaling across device densities, and crisp rendering in light/dark themes.

**Action:** Replaced system emojis in brand header, theme toggle button, and welcome placeholder state with lightweight, crisp inline SVG icons. Updated `toggleTheme` function to dynamically update SVG `path` data for sun/moon visual states.
