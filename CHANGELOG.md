# Changelog

All notable changes to the Growth Friction Index™ (GFI) platform are documented here.

---

## [Unreleased]


---

## [1.0.0] - 2026-07-22 — 🚀 Official Launch

GFI is officially live on its own dedicated domain.

### Added
- Official production launch on `gfilab.id`, with `staging.gfilab.id` for pre-release testing.

### Fixed
- **Clean URL routing (SEO-friendly URLs)** now works correctly on both production and staging, including on direct page refresh.
  - Corrected `.htaccess` `RewriteBase` / `ErrorDocument 404` config to match the root-domain deployment.
  - `js/app.js` navigation (`showInfoPage`, `showPrivacyPage`, `showTermsPage`, `goHome`) now pushes clean URLs (`/about`, `/privacy-policy`, `/terms-and-conditions`) instead of legacy `?page=` query strings.
  - Assessment result URLs now use clean format `/results/:id` instead of `?result=:id`.
  - Client-side routing now trusts server-resolved page/result detection, fixing blank content on direct-loaded or refreshed clean URLs.
  - Legacy query-string links (`?page=...`, `?result=...`) still supported for backward compatibility.

### Changed
- **Hosting migration:** moved off the shared `madebyanera.com/gfi/` subfolder onto a dedicated domain (`gfilab.id`).
- About page: hid the "100% GRATIS / 30 MENIT / ACTIONABLE PLAN" feature badges row under the consultation CTA button.

---

## [0.x] - Pre-launch (on legacy `madebyanera.com/gfi/`)

### Added
- Collapsible tooltip hints per assessment question.
- Slow-network notification pill (appears after 3s on slow connections).
- Preload hints + `defer` loading for critical JS/CSS assets.
- Auto cache-busting via `filemtime()` on all CSS/JS asset links.
- Open Graph (OG) meta tags for Privacy and Terms pages.

### Changed
- Combined the revenue calculator into a single unified 4-input screen.
- Revenue input fields made required with zero-value validation.
- All navbar logos made clickable (return to homepage).
- Footer navigation on Privacy/Terms/About pages simplified to Terms + Privacy links only.
- Share button updated to a proper share icon.
- All PNG image assets migrated to WebP for performance.
- Loading screen simplified to logo-only.

### Fixed
- Privacy Policy / Terms pages bleeding into the homepage on back-navigation.
- PDF generation failure from a 9.5MB `app.js` (base64 images crashed browser JS parsing) — resolved by externalizing PDF image assets into `js/pdf-assets.js`.
- Share link bugs: homepage loading instead of shared result; result ID sanitization allowing dots.
  
