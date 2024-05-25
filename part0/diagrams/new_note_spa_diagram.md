sequenceDiagram
    participant user
    participant browser
    participant server

    user->>browser: Write note and click "Save"
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: JSON data for the new note
    deactivate server

    Note right of browser: The browser updates the UI to include the new note without reloading the page
