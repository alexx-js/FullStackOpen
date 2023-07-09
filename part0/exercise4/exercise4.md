:::mermaid

sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Open https://studies.cs.helsinki.fi/exampleapp/notes
    Browser->>Server: Send  a request to the webpage
    Server-->>Browser: Return the webpage HTML
    User->>Browser: Write something into the input
    User->>Browser: Click Submit button
    Browser->>Server: Send POST request with the input content
    Server-->>Browser: Return success response
    Browser->>Browser: Display success message
    Browser->>Browser: Refresh the page
    Browser->>Server: Send request for the webpage
    Server-->>Browser: Return the updated webpage HTML
    Browser-->>User: Display updated webpage with new note
    
:::
