# Sarim.Khan-VCard

Professional digital visiting card (vCard) for **Sarim Khan – Project Director, FocusOn Interiors**.

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | The complete digital visiting card (single page, no build step). |
| `assets/sarim-khan.jpg` | Profile photo used on the card and embedded in the saved `.vcf`. |
| `assets/vendor/qrcode.js` | Vendored `qrcode-generator` (MIT) used to render the contact QR code offline. |

## Features

- Hero with portrait, animated background, 3D tilt and floating highlight badges
- Animated stats (₹120+ Cr directed, 4,50,000+ sq. ft. delivered, 8+ years, 5 offices)
- About, C.Q.E.T. standard, services, featured projects, marquee client list
- Contact tiles (call, WhatsApp, email, LinkedIn, portfolio, company website, offices)
- **Save Contact** button downloads a standard `.vcf` (vCard 3.0, with photo)
- **Share** button (native share sheet, falls back to copying the link)
- QR code that saves the contact directly when scanned
- Sticky quick-action dock, scroll progress bar, responsive layout, reduced-motion support

## Run locally

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

The page loads Font Awesome and Google Fonts from their CDNs, so an internet connection is needed for icons and fonts.

## Updating details

All contact details live in `index.html`:
- The `CONTACT` object and the `buildVCard()` function in the `<script>` block (used for `.vcf` and QR).
- The visible text in the HTML sections.

To change the photo, replace `assets/sarim-khan.jpg` (keep the same file name, or update the `src` and `CONTACT.photo`).
