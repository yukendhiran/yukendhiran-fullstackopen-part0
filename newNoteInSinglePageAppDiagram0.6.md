#0.6: New note in single page app diagram
```mermaid

sequenceDiagram
    participant browser
    participant server


    Note right of browser: Update DOM with new note

    Note right of browser: Convert new note into json

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    Note right of browser: Server adds new note to the page
   
    server-->>browser: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    deactivate server

    Note right of browser: New file created


```
