```mermaid
sequenceDiagram
    participant U as User
    participant B as Browser
    participant S as Server

    U->>B: Navigates to /spa
    B->>S: Sends GET request to /spa
    S->>B: Responds with HTML file (SPA shell)
    B->>S: Sends GET request for JavaScript and CSS files
    S->>B: Responds with JS and CSS files
    B->>B: Loads and executes JavaScript to render the SPA
    B->>S: Sends GET request to /data.json to fetch existing notes
    S->>B: Responds with JSON containing notes data
    B->>U: Renders notes dynamically on the page
