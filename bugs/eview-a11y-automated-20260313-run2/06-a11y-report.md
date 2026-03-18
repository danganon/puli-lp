# eView Automated On-Device Accessibility Audit (Safari on iPhone)

- Timestamp: 2026-03-13T13:47:04.708197Z
- Target: https://eview.quantclaw.org/
- Bridge Session ID: 28ce612386
- WDA Session ID: 954DB48A-1640-4C35-AA1C-672757668555
- Evidence Screenshot: `03-screen-state.png`, `04-ui-audit.png`

## Summary
- Total issues: 17
- High: 13, Medium: 3, Low: 1
- Rule counts: {"off_screen_visible": 1, "tiny_tap_target": 13, "overlapping_interactives": 2, "text_clipping_risk": 1}

## Page Confirmation Markers
- eView: True
- quantclaw: False
- Markets: True
- Heat Map: True
- Portfolio: True
- GitHub: False

## High Severity Findings (Representative)
1. `tiny_tap_target` - Interactive element is smaller than recommended 44x44 touch size.
   - Element: `Skip to main content` (link)
   - Bounds: `{'x1': 0, 'y1': 68, 'x2': 148, 'y2': 90}`
   - Details: `{'width': 148.0, 'height': 22.0}`
2. `tiny_tap_target` - Interactive element is smaller than recommended 44x44 touch size.
   - Element: `e` (link)
   - Bounds: `{'x1': 19, 'y1': 82, 'x2': 25, 'y2': 97}`
   - Details: `{'width': 6.0, 'height': 15.0}`
3. `tiny_tap_target` - Interactive element is smaller than recommended 44x44 touch size.
   - Element: `Search instruments` (text_field)
   - Bounds: `{'x1': 53, 'y1': 75, 'x2': 227, 'y2': 104}`
   - Details: `{'width': 174.0, 'height': 29.0}`
4. `tiny_tap_target` - Interactive element is smaller than recommended 44x44 touch size.
   - Element: `Keyboard shortcuts` (button)
   - Bounds: `{'x1': 317, 'y1': 76, 'x2': 344, 'y2': 103}`
   - Details: `{'width': 27.0, 'height': 27.0}`
5. `tiny_tap_target` - Interactive element is smaller than recommended 44x44 touch size.
   - Element: `Sign In` (button)
   - Bounds: `{'x1': 349, 'y1': 77, 'x2': 421, 'y2': 102}`
   - Details: `{'width': 72.0, 'height': 25.0}`
6. `tiny_tap_target` - Interactive element is smaller than recommended 44x44 touch size.
   - Element: `Launch Chart` (link)
   - Bounds: `{'x1': 160, 'y1': 417, 'x2': 260, 'y2': 440}`
   - Details: `{'width': 100.0, 'height': 23.0}`
7. `tiny_tap_target` - Interactive element is smaller than recommended 44x44 touch size.
   - Element: `Explore Markets` (link)
   - Bounds: `{'x1': 150, 'y1': 477, 'x2': 270, 'y2': 500}`
   - Details: `{'width': 120.0, 'height': 23.0}`
8. `tiny_tap_target` - Interactive element is smaller than recommended 44x44 touch size.
   - Element: `MSFT 404.04 +0.54%` (link)
   - Bounds: `{'x1': 0, 'y1': 596, 'x2': 150, 'y2': 620}`
   - Details: `{'width': 150.0, 'height': 24.0}`

## Raw Artifacts
- `00-session-create.json`
- `01-wda-status.json`
- `02-nav-response.json`
- `03-screen-state.json`
- `03-screen-state.png`
- `04-ui-audit.json`
- `04-ui-audit.png`
- `05-summary.json`