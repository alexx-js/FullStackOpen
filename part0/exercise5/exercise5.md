:::mermaid

sequenceDiagram
  participant User
  participant Browser
  participant Server

  User->>Browser: Open browser and enter URL
  Browser->>Server: Request single-page app version
  Server->>Browser: Serve single-page app
  Browser->>User: Display single-page app

  Note over User, Browser: User interacts with the app

:::