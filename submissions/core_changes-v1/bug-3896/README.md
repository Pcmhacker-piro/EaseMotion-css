# Bug 3896 — core/animations.css fixes

Fixes issue #3896

## Changes
| Selector | Original value | Fixed value |
|----------|---------------|-------------|
| `.ease-float` | `animation-duration: 3s` (hardcoded) | `var(--ease-slow)` |
| `.ease-ping` | `animation-timing: cubic-bezier(0, 0, 0.2, 1)` | `var(--ease-in-out)` |
| `.ease-rotate` | `animation-timing: linear` | `var(--ease-linear)` |

## Files
- `animations.css` — patched definitions for the three eases above.
- `README.md` — this file
