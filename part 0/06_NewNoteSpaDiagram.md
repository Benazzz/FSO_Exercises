```mermaid
sequenceDiagram
    participant browser
    participant server
	
	Note right of browser: User types a note and clicks Save
	
	browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
	Note right of server: Server appends the new note to the data store
    server-->> "201 Created"
    deactivate server
	Note right of browser: JS appends new note to DOM - no reload

```
