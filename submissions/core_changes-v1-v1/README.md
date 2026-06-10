# Fix #3957: ease-loader-ping use --ease-ease-out token

Bug: `.ease-loader-ping` hardcodes `cubic-bezier(0,0,0.2,1)` instead of `--ease-ease-out`.

## Fix
```css
.ease-loader-ping { animation: ease-kf-ping 1s var(--ease-ease-out) infinite; }
```

## Files
- `demo.html` — interactive demo
- `style.css` — the fix
- `README.md` — this file
