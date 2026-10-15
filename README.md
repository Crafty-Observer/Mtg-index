# MTG Index v0.7 Beta

Android-first GitHub Pages web app.

## Changes from v0.6
- Search field starts empty instead of `squirrel`.
- Home screen shows recent search terms (saved only in this browser) and saved decks.
- Tapping a recent search reruns it; tapping a deck opens My decks.
- Clear search history button.
- Visible v0.7 beta header and refreshed service-worker cache version.
- All existing v0.6 features and deck local-storage key retained; previously saved decks are preserved on the same origin/browser.

## Upload to GitHub Pages
Upload `index.html`, `icon.svg`, `manifest.webmanifest`, `sw.js`, and `README.md` to the repository root. `supabase-setup.sql` is for optional cloud configuration only, not required to publish.

## Notes
Searches require internet; cloud sign-in requires separate Supabase configuration. Decks stored in local browser storage should be backed up. Full functional Android testing is still required.
