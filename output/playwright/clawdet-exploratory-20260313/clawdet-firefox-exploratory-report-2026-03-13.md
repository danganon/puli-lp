# Clawdet Firefox Exploratory Report

- Date: 2026-03-13
- Browser: Firefox (Playwright Firefox engine)
- Scope: `https://clawdet.com` and `https://clawdet.com/nanofleets`
- Goal: find major UI/UX issues

## Findings (5 major UI/UX issues)

### 1. Chat widget overlaps key content on home page (mobile)
- ID: `CLAWDET-UIUX-001`
- Severity: High
- Area: Home page, mobile layout
- Steps:
1. Open `https://clawdet.com` on a mobile viewport.
2. Scroll to the feature cards section (Docker Container / Claude Sonnet / REST API / Telegram).
- Expected: Floating chat control should not cover readable content.
- Actual: Chat bubble overlaps the feature card content area.
- Evidence:
  - `07-mobile-overlap-check.png`

### 2. Sticky header clips FAQ content on NanoFleets mobile page
- ID: `CLAWDET-UIUX-002`
- Severity: High
- Area: NanoFleets FAQ section, mobile
- Steps:
1. Open `https://clawdet.com/nanofleets` on mobile viewport.
2. Scroll near the FAQ section.
- Expected: FAQ rows should remain fully visible below sticky nav.
- Actual: Top FAQ row text appears partially hidden/clipped under sticky header.
- Evidence:
  - `12-nanofleets-mobile-bottom.png`

### 3. “Log in” call-to-action on home does not navigate
- ID: `CLAWDET-UIUX-003`
- Severity: High
- Area: Home auth CTA
- Steps:
1. Open `https://clawdet.com`.
2. Click `Log in` under the sign-up card.
- Expected: User should navigate to login page.
- Actual: URL does not change, no navigation occurs.
- Evidence:
  - `08-login-text-click.png`
  - `08-login-click-result.json` (`before` and `after` URLs both `https://clawdet.com/`)

### 4. “Continue with X” leads to configuration error state
- ID: `CLAWDET-UIUX-004`
- Severity: Critical
- Area: Social sign-in / onboarding
- Steps:
1. Open `https://clawdet.com`.
2. Click `Continue with X`.
- Expected: OAuth flow should start successfully.
- Actual: Redirect ends at `https://clawdet.com/login?error=Configuration`.
- Evidence:
  - `05-after-continue-x.png`
  - `exploratory-summary.json` (`xUrl`)

### 5. Invalid signup submission fails silently (no feedback)
- ID: `CLAWDET-UIUX-005`
- Severity: High
- Area: Sign-up form validation UX
- Steps:
1. Open `https://clawdet.com`.
2. Enter invalid values (e.g., `bad-email`, short password).
3. Click `Create My Agent — Free`.
- Expected: Clear inline validation messages or visible error feedback.
- Actual: No visible error messaging and no submit network call observed.
- Evidence:
  - `06-invalid-submit-result.png`
  - `06-invalid-submit-network.json` (empty `networkLogs`)

## Artifacts folder
- `/Users/danganon/Documents/New project/output/playwright/clawdet-exploratory-20260313`
