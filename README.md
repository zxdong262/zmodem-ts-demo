# zmodem-ts-demo

A demo project showcasing [zmodem-ts](https://github.com/zxdong262/zmodem-ts) - a TypeScript implementation of the Zmodem file transfer protocol for web terminals.

This web-based terminal application connects to an SSH server via WebSocket and demonstrates Zmodem file transfers using zmodem-ts.

## About zmodem-ts

[zmodem-ts](https://github.com/zxdong262/zmodem-ts) is a TypeScript library that implements the Zmodem file transfer protocol for modern web applications. It enables reliable file transfers between web terminals and remote servers.

## Features

- Web-based terminal using xterm.js
- WebSocket connection to backend
- SSH connection to remote server
- Zmodem file transfer support using zmodem-ts

## Setup

1. Install dependencies:

   ```bash
   npm install
   ```

2. Start the Docker test server:

   ```bash
   cd src/dockers
   docker build -t zmodem-test-server .
   docker run -d -p 23355:22 --name zmodem-test zmodem-test-server
   ```

3. Start the backend:

   ```bash
   npm run backend
   ```

4. Start the frontend:

   ```bash
   npm run dev
   ```

5. Open `http://localhost:3001` in your browser.

## Project Structure

- `src/client`: Frontend React TypeScript code
- `src/server`: Backend TypeScript code
- `build/`: Build configuration
- `src/dockers/`: Docker setup for test server

## Technologies

- Frontend: React, Vite, TypeScript, xterm.js, zmodem-ts
- Backend: Express, express-ws, ssh2
- Build: Vite
- Test Server: Docker with OpenSSH

## Using zmodem-ts

This demo showcases how to integrate zmodem-ts into a web terminal application. Key implementation files:

- `src/client/zmodem/send.ts` - Sending files via Zmodem
- `src/client/zmodem/offer.ts` - Receiving files via Zmodem  
- `src/client/zmodem/addon.ts` - xterm.js addon integration

For more details on using zmodem-ts, visit the [zmodem-ts repository](https://github.com/zxdong262/zmodem-ts).
