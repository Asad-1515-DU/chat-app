# Chat App

A simple real-time chat application built with Node.js, Express, and Socket.IO. The server serves a minimal web client from `public/` and handles real-time messaging and user presence over WebSockets.

## ✅ Features

- Real-time chat using Socket.IO
- Simple web UI served from `public/` (HTML, CSS, JS)
- User join/leave notifications and user list
- Basic desktop notification support when the user is not focused
- Includes a small `test_client.js` to simulate a bot client

## 🔧 Tech stack

- Node.js (CommonJS)
- Express
- Socket.IO
- Vanilla HTML/CSS/JS for the frontend

## ⚙️ Prerequisites

- Node.js v14+ (or recent LTS) and npm

## Installation

1. Clone the repository and change directory to the `chatapp` folder:

```bash
git clone <repo-url>
cd chatapp
```

2. Install dependencies:

```bash
npm install
```

## ▶️ Running the server

Start the server:

```bash
node server.js
```

The server will listen on http://localhost:3000 by default.

Open your browser and go to http://localhost:3000, enter a username and start chatting.

## 🧪 Testing the bot client

You can run the included test bot which connects to the server as `TestBot`:

```bash
node test_client.js
```

This will connect to the running server and appear in the user list.

## 📁 Project structure

```
chatapp/
├─ server.js         # Express + Socket.IO server
├─ package.json
├─ test_client.js    # Minimal test bot using socket.io-client
└─ public/
   ├─ index.html     # Chat UI
   ├─ script.js      # Client logic
   └─ style.css      # Styling
```

## 💡 Notes

- The frontend requests desktop notification permission and will show notifications for messages when the page is not focused.
- The server stores a simple in-memory user list (not persisted). This is fine for demos but not production.

