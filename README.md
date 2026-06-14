# Trading OS

A personal pre-trade discipline + journaling system. One self-contained HTML file, no build step, no backend. It saves automatically to your browser; nothing is ever stored in this repository.

## How saving works
The app writes to your browser's local storage on every change — so it already auto-saves. Hosting it on GitHub Pages just gives it a **stable web address**, which matters because browser storage is tied to that address: push new code and your data stays put. (Opening the bare `.html` from your Downloads gives an unstable address, so data can get orphaned between versions. Hosting fixes that.)

Your data lives only in the browser you use, on that device. It does **not** sync across devices. Use **⤓ Backup** to download a JSON snapshot and **Restore** to load it — that's how you move between machines and insure against a cache wipe.

## Deploy (free, ~3 minutes, no command line)
On a free GitHub account, Pages only works from a **public** repo. That's fine here — the repo holds the app code, never your data (no trade, mark, or note is ever in the repo). Anyone with the URL could see the code, but not a single thing you've entered.

1. Create a GitHub account if you don't have one.
2. **New repository** → name it `trading-os` → Public → Create.
3. **Add file → Upload files** → drag in `index.html` (and this README) → Commit.
4. **Settings → Pages → Build and deployment → Source: Deploy from a branch** → branch `main`, folder `/ (root)` → Save.
5. Wait ~1 minute. Your site is live at `https://<your-username>.github.io/trading-os/`. Bookmark it.
   (Want the repo private? That needs GitHub Pro — but public is recommended here since no data is exposed.)

## Updating the code later
Replace `index.html` (upload a new version / commit). The page updates on next load; **your data persists** because the address and the storage key (`tradeos:db:v1`) are unchanged. Workflow: you get a new `index.html`, you upload it, data intact.

## Starting clean
Click **Reset** (top right) to erase everything in the current browser — preps, theses, watchlist, journal, daily marks — and start fresh. It asks for confirmation. Back up first if you're unsure.

## Notes
- Account P&L, recovery, and the limits run off your **daily marks** (Today tab). The journal is for process/thesis review.
- Not for sensitive transactions; it's a personal tool. Don't put anything in it you wouldn't want in a browser's local storage.
