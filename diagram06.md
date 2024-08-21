```mermaid
sequenceDiagram
    participant U as User
    participant B as Browser
    participant S as Server

    U->>B: Writes a note in the text field
    U->>B: Clicks the Save button
    B->>B: Adds the new note to the local state
    B->>S: Sends POST request to /new_note with the note data
    S->>B: Responds with confirmation and updated notes data
    B->>U: Updates the displayed list of notes without reloading the page
