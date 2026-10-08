# Faculty Atlas — Fall 2027

A static professor-outreach workspace. Open `index.html` through a web server, or use the GitHub Pages deployment. No build step or external JavaScript dependency is required.

## Use

1. Import your tracker JSON or a CSV exported from Excel. The directory starts with 67 faculty; the supplied private import retains the earlier tracker fields and adds research connections and prepared drafts.
2. Search or filter by school, topic, contact status, or follow-up date. Star faculty to shortlist them.
3. Open a professor to edit research fit, recruiting evidence, priority, notes, dates, or an email draft. Save changes.
4. Use Backup to retain the complete workspace, or Export CSV for Excel. Import a backup on another device to transfer your work.

## Data and privacy

- The public directory includes names, affiliations, research descriptions, public contact addresses, and source links. It does not contain private priorities, research hooks, contact history, notes, or email drafts.
- Personal data stays in localStorage in the current browser. There is no server-side account, GitHub writeback, automatic cross-device synchronization, email sending, analytics, or third-party asset request.
- Clearing site data or changing browser/device does not transfer your workspace. Download backups periodically.
- Use the provided private import to restore Excel priorities and prepared drafts. Original workbook tab data is retained in JSON backups; CSV exports contain the current faculty records.
- Recruiting statements imported from an earlier workbook require rechecking. A blank contact address means it has not been verified for this directory. Research match is not an admissions probability.

## Development

Run `python -m http.server 8765 --directory .` from this folder's parent, then open `/professor-tracker/`.

`core.js` holds validation, search, import/export, and follow-up logic. `app.js` renders the interface. User input is escaped in rendered HTML, external links allow only HTTP(S), and CSV output protects against spreadsheet formula interpretation.
