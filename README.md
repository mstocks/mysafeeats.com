# MySafeEats

Marketing website and brand kit for **MySafeEats**, a mobile app that helps people with celiac disease find gluten-free foods. The app scans a product's UPC barcode, pulls its ingredient list, and checks every ingredient against a list of gluten-containing ingredients, plus any allergens the person adds. It reads the ingredients first, not the front-of-package claims.

## What's here

| Path | What it is |
|---|---|
| `index.html` | The marketing site. One file with embedded CSS and JS, no build step. |
| `brand.html` | Brand guide: logo usage, palette with contrast-checked pairings, typography, components, voice and tone. |
| `logo/` | Logo files (SVG outlines, no font needed): full color, reverse, on orange, one-color, stacked, the mark, app icons (default, dark, tinted), and PNG exports. |
| `favicon.svg`, `apple-touch-icon.png` | Browser and iOS home-screen icons. |
| `og-image.png` | 1200×630 social share image. |

## Run it locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Deploy

Any static host works (GitHub Pages, Netlify, Cloudflare Pages, S3). Upload the folder as-is.

## Before launch: replace the placeholders

Search `index.html` for these (they're also listed in a comment at the top of the file):

- `[your-domain.com]`: production domain (canonical URL, Open Graph, JSON-LD, contact email)
- `[Company Name]`: legal entity in the footer
- `hello@[your-domain.com]`: contact email
- `#app-store-url`, `#google-play-url`: store listings. Swap the buttons for the official App Store and Google Play badges.
- `#privacy-policy-url`, `#terms-url`: legal pages
- `"operatingSystem"` in the JSON-LD block: confirm platforms

`og:image` needs an absolute URL, so it only works once the domain is set.

## Brand at a glance

- **Logo:** "Scan Check" mark (a check made of barcode bars on a lime circle) with an Archivo Black wordmark at 72% width.
- **Colors:** Orange `#E65E2C` (primary), Green `#245A49` (secondary), Lime `#E2EE6E` (accent), Cream `#F3E8D2` (background), Ink `#12261E` (text).
- **Type:** Archivo (Google Fonts, SIL Open Font License).
- **Results wording:** always scoped to the person's list: "Safe for your list", "Not safe for your list", "Can't check this one".

## Accessibility

Built to WCAG 2.2 AA: semantic landmarks, keyboard-friendly navigation, visible focus, color contrast checked for every text pairing, color never used alone to convey a result, and `prefers-reduced-motion` respected.

## Disclaimer

MySafeEats is a shopping aid. It does not provide medical advice and is not a substitute for reading product labels or consulting a healthcare professional. Have the site's disclaimer reviewed by a lawyer before launch.
