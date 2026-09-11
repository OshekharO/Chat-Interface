## 2023-10-24 - Canvas Visual System & Token Architecture

**Learning:** The legacy chat interface relied on hardcoded hex values and element style overrides for theme switching (`body.style.backgroundColor`). This caused major theme parity bugs where input components and message containers remained dark gray when switching to light mode. Using `data-theme="light|dark"` at the root document level tied to CSS custom properties ensures 100% theme coverage and component consistency across light and dark modes.

**Action:** Standardized all UI surfaces using tokenized CSS custom variables (`--bg-app`, `--bg-surface`, `--bg-user-msg`, `--bg-bot-msg`, `--bg-input-box`, `--border-subtle`, `--border-focus`, `--accent-primary`). Configured focus-visible indicators (`:focus-visible`) and animated thinking state indicators (`.typing-indicator`) for seamless state communication.
