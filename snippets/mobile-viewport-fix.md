# Mobile viewport fix (one line)

If your site renders ~980px wide on a phone (everything tiny, pinch-zoom needed), the page is missing the viewport meta tag. It belongs in the `<head>` of every page:

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

## How to verify (do this, do not trust the CMS preview)

1. Open the page on a real phone or in Chrome DevTools device mode (390x844).
2. The content should fit the screen width without horizontal scrolling.
3. Check the rendered source: `view-source:` and confirm the tag exists on ALL templates (home, service pages, contact) — we audited one contractor whose contact page had the text "fill out the form below" with no form and no viewport tag.

## Common gotchas

- Some page builders inject the tag only on their own templates. Check every page type.
- `initial-scale=1` matters: without it iOS may zoom arbitrarily.
- Do not use `maximum-scale=1` or `user-scalable=no` — it blocks accessibility zoom (WCAG failure).
