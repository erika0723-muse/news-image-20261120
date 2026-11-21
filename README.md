# The World in One Image — Friday 20 November 2026

Entry for the make.fun bounty **"Sum up 20 November's world news in one
image"**: a newspaper front page that sums up the world's news of Friday,
20 November 2026, in a single 1024×1024 PNG.

## The image

A classic front-page layout:

- **Masthead** naming the day in large type: *FRIDAY 20 NOVEMBER 2026*.
- **Lead story** — Russian missiles land in Poland as Kyiv's bridges are hit.
- **Eight more stories** in a two-column grid, chosen for consequence and
  breadth across regions and fields, each with a short headline and a
  one-line explainer:
  - Global markets: AI sell-off pounds world stocks (S&P 500 −3.7%, Nikkei −5.1%)
  - The Hague: ICJ finds Myanmar committed genocide against the Rohingya
  - Diplomacy: US, China & Russia issue a joint peace pledge at Shenzhen
  - Middle East: Houthi missile hits a Riyadh skyscraper
  - Peru: magnitude 6.7 earthquake in the centre of the country
  - India: Cyclone Akban makes landfall on the east coast
  - Nigeria: funeral boat capsizes in Bayelsa State
  - United States: Trump fires the National Cyber Director

Stories were selected from same-day reporting of 20 November 2026.

## How it is built

Two programs, by design:

- `render.py` — the production script. It draws the front page with
  Pillow, using the bundled DejaVu Sans fonts in `fonts/`, and writes
  `assets/entry.png`. Text is rendered programmatically (never generated
  imagery), so every letter is crisp and legible at small sizes.
  Run it with: `python3 render.py` (requires Pillow).
- `main.py` — the submitted entry program. Standard library only, no
  network: it copies `assets/entry.png` to `/output/entry.png`, creating
  `/output` if needed. Running it any number of times produces exactly
  the same bytes.

## License

MIT — see `LICENSE`. The bundled DejaVu fonts are under their own
license (Bitstream Vera / Arev derivatives, public-domain style terms).
