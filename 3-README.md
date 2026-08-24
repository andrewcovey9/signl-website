# signladvisory.com

One-page static site for Signl. (Signl Advisory). No build step: plain HTML + CSS.

- `index.html` - the whole page
- `styles.css` - design tokens taken from the Stitch export's `signal_logic/DESIGN.md`

Fonts (Geist, Inter, JetBrains Mono) load from Google Fonts. No Tailwind CDN,
no JavaScript, no hotlinked images.

## Before deploying

Every call-to-action link currently has `href="BOOKING_URL"`. Replace it with the
real booking URL in one pass:

    sed -i 's|BOOKING_URL|https://your-booking-link|g' index.html

There are 5 of them (nav, hero, closing band, footer, and the hero secondary CTA
is an in-page anchor and does not need changing).

## Deploying

Static files. Any host that serves a directory works. See the hosting notes that
came with this build for the DNS specifics at Squarespace.
