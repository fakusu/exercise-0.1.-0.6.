```mermaid
sequenceDiagram
    participant U as User
    participant B as Browser
    participant S as Server

    U->>B: Writes a note in the text field
    U->>B: Clicks the Save button
    B->>S: Sends a POST request /new_note with the note
    S->>B: Responds with success or error status
    B->>U: Displays the newly created note or an error message
