THE READING ROOM v1.1

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
