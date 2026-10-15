# MTG Index v0.6 beta — Android + PC

**Version 0.6** is visible in the app header. Upload `index.html`, `icon.svg`, `manifest.webmanifest`, and `sw.js` to the root of your GitHub Pages repository. You may also upload this README. Do **not** upload `supabase-setup.sql` to the public website; it is for the private SQL editor in your own Supabase project.

## Working without a backend
- Card search uses live Scryfall. Filters, type-priority sorting (loaded results only), double-faced flipping, printings, saved decks, preliminary validation, token inventory, Considering, swaps, JSON/text exports, and deck-share links are in the browser app.
- Local decks are private to each browser/device and are saved under the existing `mtg-index-v05` storage key, preserving v0.5 data.
- Use **Download all decks** regularly. **Import backup (merge)** does not overwrite existing decks.
- Share links contain deck data in the URL fragment, not a permanent cloud-hosted deck; large decks may exceed URL length limits. Share the app URL with friends: each person's browser storage remains separate.

## Optional cloud accounts + manual sync (requires setup)
1. Create a Supabase project at supabase.com.
2. In the project's SQL editor, run `supabase-setup.sql`. This creates the `mtg_decks` table with row-level security so each user can only access their own records.
3. In Supabase Auth settings configure the GitHub Pages site URL and email confirmation redirect. Enable email signups if desired.
4. In MTG Index → My decks → Backups and optional account sync, enter the project URL and **publishable/anon** key. Never enter a service_role/secret key.
5. Sign up, confirm email if required, sign in, then choose **Back up my decks to cloud**. On another device sign in and select **Restore/sync from cloud**. Existing local deck replacements require approval.
6. Cloud sync is **manual** in this beta, not continuous. Account and cloud storage are not active until an owner configures Supabase. Project URL/key are saved in that device's local storage; session tokens in session storage.

## Limitations
- No full offline card database, no automatic cloud conflict merging, no live multi-user editing, no permanent hosted deck page.
- Deck validation is preliminary, not tournament-grade. Token detection and printing results depend on Scryfall data.
- Card type priority sorts only loaded results. Card search requires internet.
- Not tested on a physical Android device.
