# Ledger — private, local-first expense tracker

Manual-entry expense tracker. No backend, no accounts, no SMS/bank access, no analytics, no external requests (a CSP enforces this). Data lives in your browser's IndexedDB.

## Deploy on GitHub Pages
1. Create a repo and upload these files (never commit exported backups).
2. Settings → Pages → Deploy from branch → `main` / root.
3. Open the URL on your phone → browser menu → **Add to Home Screen**.

No build step. To preview locally: `python3 -m http.server` in this folder.

## Backup & privacy
- Settings → Your data: Export JSON (full backup), Export CSV, Import backup (merges; never overwrites; duplicates skipped).
- Clearing site data erases your data: back up regularly. Backups are sensitive files.
- Static hosting means no server ever sees your data. It does not protect against a compromised device or browser.

## Model notes
Amounts are integer paise. Transfers are excluded from spending and income. Refunds: record as Income → Refund. Comparisons use same-days-last-month. "Above normal" only flags: over budget, or already >20% above the 3-month average.

## Not in v1
CSV import, rules editor (merchant → last-used category is auto-filled instead), subcategory budgets/rename/delete, category reorder/archive, merchant history page, time-of-day charts, demo data, app lock, PNG icons (iOS may show a generic icon).
