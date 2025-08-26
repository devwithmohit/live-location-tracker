# Real-Time Location Tracker 🗺️

A real-time location tracking web application built with Node.js, Socket.IO, and Leaflet Maps. Users can share their live location with others and see all connected users on an interactive map in real-time.

## ✨ Features

- **Real-time location sharing** - Instantly broadcast your location to all connected users
- **Interactive map** - Powered by Leaflet with OpenStreetMap tiles
- **Live user markers** - See all connected users as markers on the map
- **Auto-disconnect handling** - Markers are automatically removed when users disconnect
- **Responsive design** - Works on desktop and mobile devices
- **No authentication required** - Simple plug-and-play solution

## 🚀 Quick Start

### Prerequisites
- Node.js (>= 14.0.0)
- npm or yarn
- Modern web browser with geolocation support

### Installation

1. **Clone or download the project**
   ```bash
   cd your-project-folder
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the server**
   ```bash
   npm start
   ```
   or
   ```bash
   node index.js
   ```

4. **Open in browser**
   ```
   http://localhost:8080
   ```

5. **Allow location access** when prompted by your browser

## 📁 Project Structure

```
├── index.js              # Express server with Socket.IO
├── package.json           # Dependencies and scripts
├── public/
│   ├── css/
│   │   └── style.css     # Styling for the app
│   └── js/
│       └── ap.js         # Client-side JavaScript
├── views/
│   └── home.ejs          # Main HTML template
└── README.md             # This file
```

## 🛠️ How It Works

1. **Server Side** (`index.js`):
   - Express.js serves static files and renders the main page
   - Socket.IO handles real-time communication between clients
   - Listens for location updates and broadcasts them to all connected users

2. **Client Side** (`public/js/ap.js`):
   - Uses HTML5 Geolocation API to get user's current position
   - Sends location updates via Socket.IO
   - Renders an interactive map using Leaflet
   - Displays markers for all connected users

3. **Real-time Communication**:
   - `send_location` - Client sends location to server
   - `receive-location` - Server broadcasts location to all clients
   - `user-disconnected` - Server notifies when a user leaves

## 🔧 Configuration

### Default Settings
- **Port**: 8080
- **Map Provider**: OpenStreetMap
- **Location Update**: High accuracy mode
- **Timeout**: 5 seconds

### Customization
You can modify these settings in the respective files:
- Change port in `index.js`
- Adjust geolocation options in `public/js/ap.js`
- Modify map tiles or styling in `public/js/ap.js` and `public/css/style.css`

## 🌐 Browser Compatibility

- ✅ Chrome 50+
- ✅ Firefox 45+
- ✅ Safari 10+
- ✅ Edge 12+

**Note**: HTTPS is required for geolocation in production environments.

## 🚨 Troubleshooting

### Location not working?
- Ensure you allowed location access in your browser
- Check if you're using HTTPS (required for production)
- Verify geolocation is supported: `navigator.geolocation`

### Markers not appearing?
- Check browser console for JavaScript errors
- Ensure Socket.IO connection is established
- Verify the server is running on the correct port

### Can't connect to server?
- Confirm the server is running (`npm start`)
- Check if port 8080 is available
- Try accessing `http://localhost:8080` directly

## 🔒 Security & Privacy

- **Location data**: Only shared while the browser tab is active
- **No persistence**: Locations are not stored in any database
- **Anonymous**: No user identification or registration required
- **Local network**: By default, only accessible on your local machine

## 🚀 Deployment

### For Production:
1. **Enable HTTPS** (required for geolocation)
2. **Set environment variables** for port configuration
3. **Configure CORS** if needed for cross-origin requests
4. **Add rate limiting** to prevent abuse

### Example deployment platforms:
- Heroku
- Vercel
- Railway
- DigitalOcean

## 🔮 Possible Enhancements

- [ ] User authentication and profiles
- [ ] Location history and tracking
- [ ] Geofencing and alerts
- [ ] Chat functionality
- [ ] Mobile app version
- [ ] Database integration for persistence
- [ ] Multiple map layers/providers
- [ ] User clustering for performance

## 📄 License

MIT License - feel free to use this project for learning, personal use, or commercial applications.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

---

**Made with ❤️ using Node.js, Socket.IO, and Leaflet**