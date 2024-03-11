```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST as JSON data with both content and date to https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 created. JSON data is returned 
    deactivate server

    Note right of browser: The server does not ask for a redirect. Browser stays on the same page and sends no further HTTP requests.  
```

