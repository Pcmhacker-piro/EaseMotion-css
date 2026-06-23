# fix multiple modals overwriting previousFocusedElement

1. **What does this do?** Demonstrates the focus-loss bug in `core/modal.js` where opening a modal from within another modal overwrites `previousFocusedElement`, causing focus to be lost when both close. The fix uses a stack (array) to preserve focus history.

2. **How is it used?** Open `demo.html`. Click "Open Modal 1" → inside Modal 1, click "Open Modal 2" → close both. In the "broken" column, focus is lost (nowhere to tab from). In the "fixed" column, focus returns to the original trigger button.

3. **Why is it useful??
Nested or rapidly-opened modals are common in complex UIs (settings panels, confirmation dialogs, multi-step flows). Without a focus stack, keyboard users lose their place entirely. The fix is minimal — replace the single variable with an array — and fully backward-compatible.

Fixes #18792
