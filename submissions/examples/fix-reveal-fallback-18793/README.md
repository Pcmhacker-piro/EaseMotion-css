# fix reveal.js scroll-event fallback for browsers without IntersectionObserver

1. **What does this do?** Demonstrates the broken fallback in `core/reveal.js` where browsers without `IntersectionObserver` get all `ease-reveal-active` classes applied instantly on load (no animation), and shows a throttled scroll/resize listener fix that preserves the scroll-reveal effect.

2. **How is it used?** Open `demo.html`. The "broken" column shows elements appearing instantly (current fallback behavior). The "fixed" column uses a throttled scroll listener to reveal elements only when they scroll into view. Resize the window to see the resize handler in action.

3. **Why is it useful?** Browsers that don't support `IntersectionObserver` (e.g., older browsers, some WebView environments) currently see no scroll animation at all — all reveal elements are visible immediately. A lightweight scroll/resize fallback restores the reveal experience as a graceful degradation.

Fixes #18793
