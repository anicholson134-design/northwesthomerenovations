# North West Home Renovations: homepage concept

A single-page sales demo of a new homepage for North West Home Renovations (Wigan, since 1995). Only the homepage is built; links scroll within the page. Nothing is hooked up except WhatsApp:

- The quote form builds the enquiry and opens WhatsApp with it already written out (`WA_NUMBER` in the page script, set to 07500 362208, the WhatsApp number their own site links to). The visitor presses send.
- The green WhatsApp buttons (header, floating button, final call to action) open WhatsApp with a short prefilled message.

Open `index.html` in a browser, or serve the folder with any static server (`python3 -m http.server`).

## Content sources

- Copy, contact details, services and the "Why choose us" points come from northwesthomerenovations.co.uk.
- Reviews are their Google reviews as shown on their site (Trustindex widget, "Excellent, 42 reviews"), quoted word for word, without any business replies. Facebook and Instagram could not be read automatically (both refuse automated access), so nothing was taken from them yet.
- Logo: `assets/img/logo.svg` from their site (white text, orange #C67429 house, made for dark backgrounds). Brand colours follow it: orange accents on charcoal.

## Photos

All photos are their own job photos from their website (the IMG_* uploads), not the stock images their site also uses. Image slots load from `assets/img/`; a missing file shows a labelled placeholder.

The staircase slider (`case2-*`) is a real before and after of one job, from their Facebook page (sent over by Alec). The bathroom slider (`case3-*`) uses two photos from their Facebook that Alec chose as the pair. The extension slider (`case1-*`) is illustrative: a build-stage photo next to a finished room from a similar job. Quotes beside each case are genuine reviews but are not necessarily from that job.

## Hero video

`assets/video/hero.webm` / `hero.mp4` is the same free stock bricklaying footage used on the other demos (Mixkit clips 20874 and 1436, Mixkit free licence), not their own. `hero-poster.jpg` is a frame from it. It is paused for `prefers-reduced-motion`.

## Deploy

`.github/workflows/deploy.yml` publishes the repo root to GitHub Pages on every push to `main` (Pages source must be "GitHub Actions" in the repo settings).
