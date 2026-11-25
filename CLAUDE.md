# FinanceTool

Single-page farm finance records app ("My Farm | Finance Records", about v7.17 per git log): ledger, Square sales import, mileage, Schedule F / operating margins, printable reports, Google Drive sync.

## Stack and files
- `index.html` (~340 KB) holds everything: HTML, CSS, JS. No package.json, build step or tests found.
- `CNAME`: farm-finance.tstoub.com. Git remote: github.com/tstoub77/Farm_Finance.tstoub.com.
- Loads Google Fonts and Google Sign-In (`accounts.google.com/gsi/client`) from the web; uses browser `localStorage`.

## Run / deploy
- Run: open `index.html` in a browser (no dev server config found; no entry in the shared launch.json).
- Deploy: Unknown — confirm with Tim. The CNAME file suggests GitHub Pages, but no workflow or config was verified.
- Version bumps appear in commit messages (e.g. "(v7.17)"); follow that convention. Work is merged from feature branches ("Merge: ...").

## Gotchas
- Real farm financial data: `.gitignore` blocks `FarmBackup_*.json`, `Ledger_*.csv`, `Mileage_*.csv`, `Market_*.csv`, `Chase*.csv`, `*_Activity_*.csv`. Never commit exports, backups or bank statements.
- `.claude/settings.local.json` is gitignored.
- Print layout (cover page, "Page X of Y" footer) has had repeated fixes; check the printed report after layout changes.
