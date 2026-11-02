THE READING ROOM v0.9

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
