## 2025-09-12 - Live Typing Indicator Announcements in Injected Chat Nodes
**Learning:** Dynamic typing indicators injected via `innerHTML` into chat containers do not announce state changes to screen readers unless the container explicitly includes `role="status" aria-live="polite"` and an informative `aria-label`.
**Action:** When dynamically appending typing indicator placeholders in vanilla JS chat applications, include inline ARIA live attributes on the container element at creation time.
