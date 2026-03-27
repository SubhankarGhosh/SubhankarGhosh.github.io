# Font Update Log: Changing to Inter

Date: 2026-03-23

## Changes to `_includes/head.html`
Added the following Google Fonts import links before the main stylesheet to load the Inter font:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

## Changes to `_sass/_variables.scss`
Updated the `$sans-serif` variable to prepend `"Inter"` to the font stack:
**Before:**
```scss
$sans-serif: -apple-system, ".SFNSText-Regular", "San Francisco", "Roboto", "Segoe UI", "Helvetica Neue", "Lucida Grande", Arial, sans-serif;
```
**After:**
```scss
$sans-serif: "Inter", -apple-system, ".SFNSText-Regular", "San Francisco", "Roboto", "Segoe UI", "Helvetica Neue", "Lucida Grande", Arial, sans-serif;
```

If you ever need to revert, simply remove the Google Fonts lines from `_includes/head.html` and remove `"Inter", ` from the `$sans-serif` definition in `_sass/_variables.scss`.
