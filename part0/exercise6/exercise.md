:::mermaid 

sequenceDiagram
  participant User
  participant Browser
  participant Server

  User->>Browser: Open browser and enter in the page
  Browser->>Server: Request single-page app version
  Server->>Browser: Serve single-page app
  Browser->>User: Display single-page app

  Note over User, Browser: User interacts with the app

  User->>Browser: Fill in the note input
  Browser->>Browser: Generate JSON data
  Browser->>Server: Send POST request to new_note_spa
  Server->>Server: Parse JSON data
  Server->>Server: Create new note
  Server->>Browser: Return status code 201 created
  Browser->>User: Display success message

  Note over Server: New note creation process

:::