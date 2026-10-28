# Measure Up Contracting Inc.: website

A one-page website for Measure Up Contracting Inc., an owner-led residential renovation company serving the Greater Toronto Area. It's plain HTML, CSS and JavaScript with no build step, so it runs on GitHub Pages as-is.

Live: https://jdix22.github.io/measure-up/

## Highlights
- **Before/after sliders** built from the company's own Instagram photos: one in the hero that wipes across on load, and a showcase of six projects (bathroom, mudroom, foyer, deck, two gates). Drag with a mouse, swipe on a phone or use the arrow keys.
- Black-and-gold look taken from the logo, with a tape-measure motif
- Services, process, about the owner, photo gallery with a full-size viewer, FAQ and an estimate form
- The estimate form needs no server: it opens the visitor's email app with their details filled in, addressed to measureupcontractinginc@yahoo.com
- A sticky "Call / Free estimate" bar on phones
- SEO basics: meta description, Open Graph tags and `GeneralContractor` structured data (JSON-LD)

## Files
- `index.html`: the whole site
- `assets/img/`: project photos (cropped from Instagram) and the logo cut out on a transparent background

## Editing
- **Projects in the before/after showcase:** edit the `projects` array near the bottom of `index.html`. Each project uses `assets/img/<key>-before.jpg` and `<key>-after.jpg`; `ar` is the photo's width divided by its height. Pairs shot from the same angle look best.
- **Phone / email:** search `index.html` for `6472131448`, `213-1448` and `measureupcontractinginc@yahoo.com`, and update the JSON-LD block in `<head>`.
- **Colours:** change the CSS variables at the top of `<style>` (`--gold` is the accent).
- **Form to inbox instead of email app:** point the form at a service like Formspree (`<form action="https://formspree.io/f/XXXX" method="POST">`) and remove the `mailto` handler in the script.
