# Granite Cut Simulator — supplier demonstration

A mobile-first, static HTML prototype of a customer-directed granite furniture designer. **This is a demonstration, not a fabrication-ready configurator or real storefront.**

## Try locally

Open `index.html` for a quick preview, or run `python3 -m http.server 8000` in the project folder and visit `http://localhost:8000`. For camera permissions on a phone, publish to an HTTPS origin.

## Upload to GitHub (no command line)

1. Create a new repository on GitHub, e.g. `granite-cut-simulator`.
2. Choose **Public** if you want to use GitHub Pages without checking plan limitations; **Private** is possible, but Pages availability depends on your account/plan.
3. On the empty repository, choose **uploading an existing file** and upload the **contents of this ZIP**, keeping `index.html`, `catalog.json`, `textures/`, and `.github/workflows/pages.yml` in their original paths. GitHub's browser uploader may not preserve hidden directories reliably; if that happens, use GitHub Desktop or a Git client to push the unzipped folder.
4. In **Settings → Pages → Build and deployment**, choose **GitHub Actions**.
5. Push to the `main` branch. The Pages workflow will deploy the site; find its HTTPS URL in the Pages settings or Actions run.

For the simplest alternative, you can publish the static files on Netlify Drop or Cloudflare Pages. GitHub Pages hosts static assets only and cannot run a private checkout backend.

## Current prototype

- Cinematic entrance and mobile-first interface
- 30 generated, granite-inspired textures in `textures/` with metadata in `catalog.json`
- Touch-focused visual shape editing and design export
- Stylized room / furniture preview and base selection
- Camera permission and live overlay demonstration (not anchored AR)
- Illustrative pricing and local-only mock order flow

## Integration contracts

- `catalog.json` contains sample IDs, names, relative image paths, and placeholder supplier fields.
- Replace procedural textures with **licensed, verified photos of actual supplier slabs**, plus SKU, stock, lead time, pricing, and finishes.
- Exported design JSON is **not** fabrication CAD. A fabricator must validate geometry, tolerances, seam positions, material thickness, support, and feasibility before quoting.
- Checkout is **mock only**. Add a backend with inventory validation, quoting, tax/shipping, payment processor, and order tracking before accepting money.
- Camera mode is a 2D overlay; production AR needs supported device tracking, scale calibration, and spatial anchors.

## Testing status

Packaging, local references, catalog entries, and JavaScript syntax are checked as part of this delivery. A live iPhone, camera, or end-to-end checkout test has **not** been completed.
