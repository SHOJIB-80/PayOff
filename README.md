# PAYOFF — Growth, measured

A responsive, editorial marketing-agency website built with plain HTML, CSS and JavaScript. The design combines a concise commercial point of view, useful conversion paths, accessible disclosure/navigation behavior, and licensed photography. All unverified business details remain explicitly editable placeholders.

## Run the downloadable website

1. Extract the `PAYOFF-Website.zip` archive.
2. From the `PAYOFF-Website` folder, run:

   ```bash
   python3 -m http.server 8000
   ```

3. Open `http://localhost:8000` in a browser.

The downloadable copy uses local WebP files under `assets/images/`, so its photography works without Manus project storage. The live Manus project source uses its uploaded `/manus-storage/` paths; use the Manus Preview for that copy.

## Project files

- `index.html` — the complete one-page website and editable content.
- `styles.css` — brand tokens, responsive layout, image crops, accessibility and reduced-motion rules.
- `script.js` — lightweight menu, scroll-state and disclosure behavior.
- `manus-routes.json` — static route declaration for `/`.
- `assets/payoff-mark.svg` — PAYOFF brand mark and favicon.
- `assets/images/` — six optimized, locally packaged Pexels photographs.
- `assets/image-sources.md` — source pages, photographer credits, license and placement notes.
- `docs/elementor-novamira.md` — per-section rebuild notes, image mapping, crop guidance and replace-before-launch list; the Manus project keeps this file at its root.
- `docs/plan.md` and `docs/TODO.md` — approved design plan and delivery state; both sit under `docs/` in the ZIP and at the project root in Manus.
- `app.config.ts` — Manus project metadata; it is not needed by the standalone local website.

## Before public launch

Replace the `#booking-destination` placeholder with the real scheduling/contact URL, confirm the working agency name, and replace all bracketed client, result, testimonial, team and policy placeholders with approved facts. Stock photos are illustrative only: they do not depict PAYOFF staff, clients, case-study work or endorsement. The source ledger contains the Pexels license reference and image credits.
