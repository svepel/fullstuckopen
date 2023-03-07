## Exersise 0.6: New note in Single page app diagram

```mermaid
sequenceDiagram
    participant browser
    participant server
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of browser: Request contains the new note as JSON data containing 'content' and 'date'
    
    server-->>browser: [{"message":"note created"}]
    deactivate server

    Note right of browser: The server responds with status code 201 created. The browser stays on the same page, and it sends no further HTTP requests.
    

```
