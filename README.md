# Real-Time Tracker (Node.js + Leaflet)

A simple real-time location tracker built with Node.js, Socket.IO and Leaflet. The app shares each connected client's current geolocation to all other clients and displays them on an interactive map.

## Features
- Real-time location broadcast using Socket.IO
- Interactive map display with Leaflet
- Per-client markers that update or remove on connect/disconnect
- Minimal, easy-to-run example suitable for learning or extension

## Prerequisites
- Node.js (>= 14)
- npm

## Quick start
1. Open a terminal in this folder:
   - Windows (PowerShell/CMD): `cd c:\Users\ronni\Project_folder\project-1\realTime-tracker\01_folder`
2. Install dependencies:
   ```
   npm install
   ```
3. Start the server:
   ```
   npm start
   ```
   or
   ```
   node index.js
   ```
4. Open a browser to:
   ```
   http://localhost:8080
   ```
   Allow location access when prompted.

## Project structure
- index.js — server (Express + Socket.IO)
- public/ — client assets
  - js/ap.js — client logic (geolocation + Socket.IO)
  - css/style.css — styles
- views/home.ejs — HTML template
- README.md — this file

## Notes & troubleshooting
- Geolocation requires a secure context (HTTPS) on most browsers. For local testing, `http://localhost` is allowed, but production must use HTTPS.
- If location is not sent:
  - Ensure you allowed location in the browser.
  - Check browser console for errors.
  - Confirm server is running and Socket.IO client connects (browser network tab).
- If markers don't appear or move, ensure ap.js emits the same socket event names the server listens for (e.g., `send_location` / `receive-location`) and that Leaflet `setLatLng` is called with [lat, lng] array.

## Extending
- Add authentication to identify users
- Persist location history in a database
- Add map clustering for many users
- Secure with HTTPS and CORS configuration

## License
MIT — modify as needed.

```<!-- filepath: c:\Users\ronni\Project_folder\project-1\realTime-tracker\01_folder\README.md -->
# Real-Time Tracker (Node.js + Leaflet)

A simple real-time location tracker built with Node.js, Socket.IO and Leaflet. The app shares each connected client's current geolocation to all other clients and displays them on an interactive map.

## Features
- Real-time location broadcast using Socket.IO
- Interactive map display with Leaflet
- Per-client markers that update or remove on connect/disconnect
- Minimal, easy-to-run example suitable for learning or extension

## Prerequisites
- Node.js (>= 14)
- npm

## Quick start
1. Open a terminal in this folder:
   - Windows (PowerShell/CMD): `cd c:\Users\ronni\Project_folder\project-1\realTime-tracker\01_folder`
2. Install dependencies:
   ```
   npm install
   ```
3. Start the server:
   ```
   npm start
   ```
   or
   ```
   node index.js
   ```
4. Open a browser to:
   ```
   http://localhost:8080
   ```
   Allow location access when prompted.

## Project structure
- index.js — server (Express + Socket.IO)
- public/ — client assets
  - js/ap.js — client logic (geolocation + Socket.IO)
  - css/style.css — styles
- views/home.ejs — HTML template
- README.md — this file

## Notes & troubleshooting
- Geolocation requires a secure context (HTTPS) on most browsers. For local testing, `http://localhost` is allowed, but production must use HTTPS.
- If location is not sent:
  - Ensure you allowed location in the browser.
  - Check browser console for errors.
  - Confirm server is running and Socket.IO client connects (browser network tab).
- If markers don't appear or move, ensure ap.js emits the same socket event names the server listens for (e.g., `send_location` / `receive-location`) and that Leaflet `setLatLng` is called with [lat, lng] array.

## Extending
- Add authentication to identify users
- Persist location history in a database
- Add map clustering for many users
- Secure with HTTPS and CORS configuration

## License
