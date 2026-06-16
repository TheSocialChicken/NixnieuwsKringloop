# Nix Nieuws Kringloop – Project Plan

## Store Info
- **Name:** Nix Nieuws Kringloop & Vintage
- **Address:** Veerplein 27, 1404 DA Bussum
- **Phone:** +31 6 15 02 69 29
- **Instagram:** [@nix_nieuws](https://www.instagram.com/nix_nieuws)
- **Maps:** https://maps.app.goo.gl/BTLDWL3Zdxf4bfLP9
- **Domain:** nixnieuws.nl

## Tech Stack
- Pure static HTML/CSS — no build step, no framework
- Hosted on GitHub Pages (TheSocialChicken/NixnieuwsKringloop)
- Deployed via GitHub Actions on push to `main`
- Push access via SSH (kamitor account)

## Design System
- **Skill:** `artistic` from typeui.sh
- **Style:** Art Deco / theatrical vintage — fits "kringloop en vintage" brand
- **Primary font:** Limelight (Google Fonts) — Art Deco display
- **Body font:** Inter
- **Colors (adapted from skill — warm vintage palette):**
  - Cream: #F7F0E3
  - Gold: #B8860B / #D4A843
  - Brown: #3D2B1F
  - White: #FFFEF8

## Site Sections
1. **Header** — Store name in Limelight, Art Deco geometric background
2. **Contact & Route** — Click-to-call phone, Google Maps navigation button
3. **Openingstijden** — Opening hours (TODO: confirm with owner)
4. **Instagram** — Link to @nix_nieuws + Instagram feed widget

## Still Needed
- [ ] Opening hours — not available online, ask store owner
- [ ] Instagram feed widget — owner needs to connect Instagram to LightWidget or SnapWidget (one-time OAuth, then embed code works automatically)
- [ ] DNS setup for nixnieuws.nl — Thomas configures:
  - A records: 185.199.108.153 / .109 / .110 / .111
  - CNAME www → thesocialchicken.github.io
  - Then enable "Enforce HTTPS" in repo Settings → Pages

## Deploy Pipeline
```
push to main → GitHub Actions (deploy.yml) → GitHub Pages
URL: https://thesocialchicken.github.io/NixnieuwsKringloop/
Custom: https://nixnieuws.nl/ (after DNS)
```
