# Fix #3958: ease-loader-spin use timing token

Bug: `.ease-loader-spin` hardcodes `linear` timing. Fix: use `var(--ease-timing-linear)` token (to be added to core/variables.css).

## Files
- demo.html, style.css, README.md, loader-spin-token.css
