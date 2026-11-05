THE READING ROOM v1.2

Upload the contents of this folder to your GitHub Pages repository. Keep ReadingRoom_Tracker_Import.json private and do NOT upload it to the public repository.

v0.9 adds Reading History and a private tracker JSON import. Import ReadingRoom_Tracker_Import.json from Settings or Reading History. Demo seed entries are removed; other books you added are retained and matched by title/author where possible.

The import preserves all 19 completed-reading entries, six TBR/library entries, month-only dates, blank formats, ratings, read type, reviews, ownership and notes. It does not invent exact days or unknown formats. Senlin Ascends remains qualitative profile context, not a dated/rated completion.

Download backup preserves tracker data and books. Export for Scriptable remains schemaVersion 2 and exports the book list for compatibility. Data stays in browser local storage.


VERSION 1.0 - HYBRID READING HISTORY
- Reading History now combines overview statistics with the chronological log.
- KPI cards show completed entries, five-star entries, average recorded rating, and reread entries.
- Rating distribution and recent month-level activity are calculated from imported tracker data.
- Year, rating, and read-type filters narrow the history log.
- Unknown dates, ratings, and formats remain unknown; charts use only recorded data.
- Tracker data remains local to the browser and is not included in the public website files.


VERSION 1.1 - INTERACTIVE READING HISTORY
- Summary cards are tappable: Completed entries and Average rating clear the rating, read-type and month filters; Five-star and Reread entries filter the log (tap again to clear).
- Rating bars (5-1 stars and Unrated) filter the log; tap the selected bar again to clear.
- Monthly activity bars filter by completion month; tap again to clear. Only recorded completion months are charted; undated entries are never given a date.
- Year selector (All years + every year in the tracker) scopes the cards, charts and log. Rating/read-type filters persist across year changes; a month filter outside the new year is cleared.
- New Month dropdown and a "Reset all filters" button. All filters combine.
- Log is newest first, with a "Showing X of Y entries for <year>" count and an empty state with a reset button.
- No data-model, localStorage key, backup, or Scriptable export changes. No tracker re-import needed. Filters are view-only and are not saved.

UPGRADING FROM v1.0: replace index.html in your GitHub repo with this one. Keep your private tracker/library JSON files out of the repo.


VERSION 1.2 - LOG A BOOK + COVER-ART WIDGET
APP
- "+ Log a book" (Reading History tab): title, author, month finished (optional, never guessed), rating (or unrated), first read/reread, format, review. Optionally marks the book Completed in your library (adds it if new; never demotes Hall of Fame).
- Entries logged in the app are tagged source:"app" and labelled "Logged in app". Only these can be edited or deleted. Imported tracker records are read-only and untouched.
- Re-importing your tracker keeps your app-logged entries. Backup/restore include them. They do not appear in the Scriptable export (books only), so the export format is unchanged.
- Book dialog: "Find cover automatically" looks up an exact title match on Open Library and fills the Cover URL (review it, then Save).
WIDGET (ReadingRoom_Widget_v12.js)
- Uses the v0.4 cozy-shelf look and reads your exported library.json from On My iPhone / Scriptable / ReadingRoom / library.json. The widget uses Scriptable local storage, not iCloud, so it does not require available iCloud storage.
- Covers: the book's coverURL, else its ISBN, else an Open Library title/author lookup. Images are cached on the phone; missing covers fall back to the v0.4 spine/front art.
- Widget parameter: collection and page, e.g. reading, favorites, tbr, "tbr 1", "reading:daily". Empty parameter = Currently Reading.
SETUP: in Scriptable, create a new script named "Reading Room", paste in ReadingRoom_Widget_v12.js, then export from the app and save library.json to On My iPhone / Scriptable / ReadingRoom. In the Files app, choose Browse > On My iPhone > Scriptable, create a ReadingRoom folder if needed, and place library.json inside it. The older ReadingRoom_Widget_v06.js is still included.
UPGRADING: replace index.html in your GitHub repo. No re-import needed.


VERSION 1.2.1 - SHELF CAPTION POLISH
- Shelf books use a consistent caption width and a three-line title limit, with an ellipsis for exceptionally long titles.
- Full titles remain available as the book button accessible label and title, and opening the book still shows its full details.
- No data-model, localStorage, backup, tracker-import, or Scriptable-export changes.


V1.2.2 UPDATE
- Scriptable widget now reads library.json from FileManager.local(): On My iPhone / Scriptable / ReadingRoom / library.json. No iCloud download or available iCloud storage is required.
- Cover image cache remains in Scriptable local storage under ReadingRoomArt.


VERSION 1.2.3 - APP-MANAGED SCRIPTABLE WIDGET
- Settings now includes widget collection, heading, tap destination, page behavior, refresh interval, automatic cover lookup, and decorative bookend controls.
- Update Widget launches the installed Scriptable app through its URL scheme and sends the current library plus widget settings. Scriptable writes both into its local On My iPhone storage; no iCloud Drive or manual JSON transfer is required for this handoff.
- Scriptable stores widget settings in ReadingRoom/widget-settings.json and library data in ReadingRoom/library.json. Cover cache remains in ReadingRoomArt.
- Existing widget parameters can still override the selected collection/page.
- Manual library.json download remains available as a fallback.
- No tracker history or personal review data is sent; only the library books and widget display settings are transferred.
- The direct URL handoff has a payload-size guard. Very large libraries should use the manual JSON export.
