# The Tarot — deploy & install

Upload **everything in this folder** to a static host, keeping the
filenames and the `cards/` folder structure exactly as-is.

## GitHub Pages
1. New repo → upload all files **and the `cards/` folder** to the repo
   root (not a subfolder).
2. Settings → Pages → Deploy from branch → `main` / `/ (root)`.
3. Live at `https://yourusername.github.io/repo-name/`

If your repo is private, GitHub Pages requires a paid plan — either
make the repo public (Settings → Danger Zone → Change visibility),
or use Netlify Drop instead (https://app.netlify.com/drop — drag the
whole folder, no account needed).

## Add to home screen
- **iPhone (Safari):** open the URL → Share → "Add to Home Screen."
- **Android (Chrome):** an "Install this app" prompt appears in-app.

Opens full-screen with no browser bar, and works offline after the
first time you view each card.

## How the app works

**1 Card** (default tab) — a card back sits center-screen. Tap it to
browse all 78 cards grouped by suit, or type a name (or a number —
`13` finds Death, `3` finds the Empress and the Threes) in the box
below. Either way the card flips face-up and its full reading appears
underneath.

**Quiz Me** — tap the card back to flip to a random card. Tap
**Reveal Meaning** to see the full write-up. **Next Card** deals
another; the deck runs through all 78 without repeats before
reshuffling.

**Spreads** — pick a spread from the dropdown. The table shows every
position as a face-down card, laid out the way it would sit on an
actual reading table (the Celtic Cross renders as a real cross, with
the crossing card laid sideways over the covering card). Tap any
position to choose its card, or use the text box for that position
below — either fills the other. Once every position is filled, the
full multi-card reading (dignities, resonance, narrative) appears.
**Custom spread…** lets you add and label positions one at a time.

## After editing index.html
Bump the cache version in `sw.js` so installed copies pick up the
change instead of serving a stale one:
```js
const CACHE = 'the-tarot-v4';   // was v3
```
