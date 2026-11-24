# Tom — Cebu Gold Scrap Buyer daily boards

Public, direct-download host for the daily Facebook price-board PNGs.
Buffer fetches these as raw image URLs.

## URLs to use in Buffer `assets.image.url`

Prefer the dated path so caches do not serve yesterday's board:

- Dated: `https://raw.githubusercontent.com/Narvin17/tom-cebu-gold-daily/main/boards/YYYY-MM-DD.png`
- Latest: `https://raw.githubusercontent.com/Narvin17/tom-cebu-gold-daily/main/latest.png`

A curl check should show `Content-Type: image/png` and a PNG magic header, not an HTML page.

## How a new board is published here

The GitHub file tools only accept text, so the routine commits a Base64 copy (`.png.b64`). The Action in `.github/workflows/decode-png.yml` decodes it to a real PNG and pushes that file.
