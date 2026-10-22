# Releasing an update to Ballot Counter

Players' data is stored on each phone, separately from these files, so replacing the files does NOT erase anyone's data.

## Before you release
1. Ask the client to tap **Download → Backup App** (takes a few seconds).
2. Never rename the GitHub repo or move the site to a new web address. Data is saved per address; a new address starts empty (restore from the Backup App file if it ever has to move).

## To release
1. Open `index.html`. Near the top of the script, change:
   - `APP_VERSION` (e.g. `'1.1'`)
   - add a new entry at the TOP of `VERSION_HISTORY`, e.g.
     `{v:'1.1',date:'October 2026',notes:['Fixed the Reconciliation formula.']}`
2. In GitHub: open the repo, drag the new `index.html` onto the page (Add file → Upload files), Commit. The site updates in about a minute.
3. Ask the client to open the app once while online. They will see an "App updated" message listing what's new.

## Good to know
- Totals are recalculated from the typed-in numbers every time, so a formula fix corrects ALL past days on screen and in new exports. Texts already sent and pictures already saved to Photos are unchanged.
- If you change how data is stored (not just formulas), add a conversion step first so old data carries forward.
- Keep version `1.0` until the client has started using the app.
