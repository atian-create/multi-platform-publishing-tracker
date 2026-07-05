# Multi-platform Publishing Tracker

A simple local-first publishing checklist for creators, indie teams, and content operators who repurpose one idea across many platforms.

It is a single-page web app. No signup, no database, no backend required. Open it in a browser and your data is saved in Local Storage.

![Tracker overview](assets/screenshots/overview.png)

## What It Does

- Track one content idea across multiple platforms and accounts.
- Click cells to mark where a piece has already been published.
- Edit platform account names directly in the table header.
- Add or delete platform/account columns.
- Add notes or performance labels to each content row.
- Collapse months to focus on recent work.
- Export and import CSV files.

## Why This Exists

Most content teams do not need a complex project management system for distribution. They need a visible grid:

- rows = content ideas or projects
- columns = platforms and accounts
- checkmarks = already published

This project is intentionally small so people can adapt it to their own workflow.

## Quick Start

Option 1: open directly

```bash
open index.html
```

Option 2: run a local server

```bash
python3 -m http.server 8765
```

Then open:

```text
http://127.0.0.1:8765/
```

## How To Customize

1. Click `Platform +` to add your own platform group and account.
2. Click any account name in the table header to rename it.
3. Click `Add content` to add a new content idea.
4. Click a cell when that content has been published to that account.
5. Use `Export CSV` for backup or spreadsheet editing.

## Privacy

The app stores data in your browser's Local Storage. It does not send your content anywhere.

If you clear browser data, Local Storage may be removed. Export a CSV backup if the tracker matters to you.

## Screenshots

### Overview

![Overview](assets/screenshots/overview.png)

### Editing Account Names

![Edit account names](assets/screenshots/edit-accounts.png)

### Add or Delete Accounts

![Account management](assets/screenshots/account-management.png)

## Files

- `index.html` - the full app
- `REDDIT_POST.md` - suggested Reddit post copy
- `assets/screenshots/` - clean demo screenshots

## License

MIT
