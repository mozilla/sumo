# Mobile UI Fix for Revisions Page

## Issue Description
Fix for [Issue #2525](https://github.com/mozilla/sumo/issues/2525): The "Bots" checkbox is not positioned correctly inside the /revisions page on mobile devices.

**Problem:**
- The "Bots" checkbox appears in the center of the screen instead of next to its label
- The "Start:" label doesn't wrap to a new line as expected on mobile devices
- The form layout breaks on mobile, making it difficult to use

## Files in this fix

### 1. `mobile-revisions-fix.css`
CSS patch that fixes the mobile layout issues for the revision filter form.

**Key fixes:**
- Overrides the `inline-label` flex layout on mobile screens (≤768px)
- Forces form fields to stack vertically on mobile
- Properly positions the "Bots" checkbox next to its label
- Ensures the "Start:" label appears on its own line
- Makes the form responsive and user-friendly on mobile devices

### 2. `recent_revisions_mobile_fix.html`
Improved HTML template structure for better mobile layout support.

**Improvements:**
- Adds wrapper divs for better field grouping
- Ensures proper semantic structure for mobile accessibility
- Maintains backward compatibility with existing functionality

## How to Apply the Fix

### For Kitsune Repository:

1. **Apply the CSS fix:**
   Copy the contents of `mobile-revisions-fix.css` to:
   ```
   kitsune/sumo/static/sumo/scss/components/_revisions-mobile.scss
   ```
   
   Or add the CSS rules to the existing form fields SCSS file:
   ```
   kitsune/sumo/static/sumo/scss/base/forms/_fields.scss
   ```

2. **Update the template (optional):**
   Apply the structural improvements from `recent_revisions_mobile_fix.html` to:
   ```
   kitsune/wiki/jinja2/wiki/recent_revisions.html
   ```

### Testing

To test the fix:

1. Navigate to `/en-US/kb/revisions` on a mobile device or mobile emulator
2. Verify that:
   - The "Bots:" checkbox appears next to its label (not in the center)
   - The "Start:" label appears on its own line
   - All form fields are properly aligned and usable on mobile
   - The form maintains functionality on desktop

## Technical Details

The root cause was that the `.inline-label` CSS class uses `display: flex` which works well on desktop but breaks on mobile screens. The fix:

1. Uses CSS media queries to detect mobile screens (max-width: 768px)
2. Overrides the flex layout with block layout on mobile
3. Specifically targets the revision filter form (`.filter.inline-label.is-condensed`)
4. Applies special handling for checkbox fields to maintain proper alignment
5. Forces labels and inputs to stack vertically on mobile

## Browser Compatibility

This fix is compatible with:
- iOS Safari 12+
- Chrome Mobile 70+
- Firefox Mobile 68+
- Samsung Internet 10+

## Related Issues

- Fixes #2525 - [Mobile] The "Bots" checkbox is not positioned correctly inside the /revisions page on mobile devices