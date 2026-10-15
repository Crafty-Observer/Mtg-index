# MTG Index v0.3 — Android + PC web prototype

## Deploy from Android (GitHub Pages)
1. Sign in to github.com and create a **public** repository named `mtg-index`.
2. Upload **index.html**, **icon.svg**, **manifest.webmanifest**, and **sw.js** to the repository root (not the ZIP itself).
3. Open repository **Settings → Pages → Build and deployment**, choose **Deploy from a branch**, **main**, and **/(root)**, then save.
4. Once GitHub Pages publishes, open `https://YOUR-USERNAME.github.io/mtg-index/` on Android Chrome. Open Chrome's menu and choose **Install app** or **Add to Home screen**.

## Capabilities
- Live Scryfall card searches; type `squirrel` to match card types or Oracle rules text.
- Category chips perform server-side Scryfall searches, so category results are not restricted to the first page loaded. Creature searches use type filters; token and support categories are broad text searches, **not guaranteed semantic classification**.
- Combined format, color identity, type, mana value, set, sorting, and unique card/art/printing filters.
- Load more paginated search results; view a card and the first page of its printings.
- Installable mobile-first PWA, also works on PC browsers.

## Not yet implemented
No APK, no complete offline database, no saved deck builder, no deployment or hosting included. Searches require internet and Scryfall availability. API rate limits and terms apply. GitHub Pages is public hosting: don't put API keys or secrets in the repository.
