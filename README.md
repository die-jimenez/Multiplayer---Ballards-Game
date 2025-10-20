# Server-BallardsGame
Repositories
- **Server/WebApp:** [Server-BallardsGame](https://github.com/die-jimenez/Server-BallardsGame)
- **Unity Project:** [Multiplayer-Ballards-Game](https://github.com/die-jimenez/Multiplayer---Ballards-Game)

## Setup and Usage

### First time setup

1. **Install Node.js**
2. Open terminal in the project's root folder and run:
```bash
   npm install
```

### Running the project

1. Start the server:
```bash
   npm start
```

2. Open `index.html` with Live Server (or similar local hosting tool)
3. Open the Unity project and enter Play Mode
4. Press the **Connect** button in Unity to connect to the server (default: `ws://localhost:3000`)
5. Test the cube's color by pressing the **Send** button in the browser
> **Note:** You can replace `localhost` with the IP address of the machine running the server if needed.

---

## Design and Architecture

### Communication Protocol

The project uses **WebSocket** for communication between Unity and the server.

Messages follow a command-based structure in JSON format:
```json
{
  "command": "command_name",
  "attribute": { }
}
```

This event-driven design provides a standardized way for clients to communicate with the server.

### Production Considerations

** This is a local development project.** It lacks production-ready features such as:
- Authentication and authorization
- Encrypted communications (WSS)

The command-based architecture makes it easy to extend and maintain for future improvements.
