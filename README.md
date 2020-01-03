Note Taker application is used to write, save, and delete notes. This application used an express backend and save and retrieve note data from a JSON file.

The following HTML routes hadled by this app:

  * GET `/notes` - returns the `notes.html` file.

  * GET `*` - returns the `index.html` file

The application have a `db.json` file on the backend that is used to store and retrieve notes using the `fs` module.

The following API routes hadled by this app::

  * GET `/api/notes` - reads the `db.json` file and returns all saved notes as JSON.

  * POST `/api/notes` - recieves a new note to save on the request body, adds it to the `db.json` file, and then returns the new note to the client.

  * DELETE `/api/notes/:id` - recieves a query paramter containing the id of a note to delete. In order to delete a note, app reads all notes from the `db.json` file, removes the note with the given `id` property, and then rewrites the notes to the `db.json` file.