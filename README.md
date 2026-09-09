# lucky-spin

A single-page **Titan / Fastrack demo** built for a 1080×1920 portrait kiosk. No build step,
no backend — just static HTML/CSS/JS.

## Pages

| Tab | What it does |
|---|---|
| **Watches** | Full-screen auto-rotating carousel of Fastrack campaign & collection banners. |
| **Lucky Spin** | Enter mobile number → OTP (`1234` for the demo) → spin the wheel for an instant offer code. "Start again" sends the next person back through login. |
| **Play & Win** | *Titan Time Rush* — an embedded catch-the-watches mini-game with a bonus discount code at the end. |
| **Products** | 8 Fastrack watches with photos, prices and a detail popup. |

## Run it

```bash
npx serve . -l 4599
```

Then open <http://localhost:4599>. For the kiosk, load it full-screen on a 1080×1920 portrait display.

## Deploy

Static site — deployed on Netlify from `main` (publish directory: repo root, see `netlify.toml`).

## Files

- `index.html` — the whole site (carousel, spin wheel, product grid, modal).
- `game.html` — the standalone *Titan Time Rush* game (embedded by the Play & Win page).

## Notes

- Product images, names and prices are pulled from fastrack.in for demonstration only.
- The OTP code is hard-coded to `1234`; no SMS is sent and no offer is redeemable.
