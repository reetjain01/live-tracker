# Live Tracker

A Real-Time location tracking web application using Leaflet for mapping and Socket.IO for real-time communication. This application displays user locations on a map and updates in real-time as users move.

## Features

- Real-time location tracking with Leaflet.
- Dynamic map updates based on user location.
- Real-time updates of user positions using Socket.IO.
- Marker management for connected users and removal upon disconnection.

## Technologies

- **Backend**: Node.js, Express, Socket.IO
- **Frontend**: HTML, EJS, Leaflet.js
- **Real-time Communication**: Socket.IO
- **Mapping**: Leaflet.js

## Installation

### Prerequisites

- Node.js and npm (Node Package Manager)

### Steps

1. **Clone the repository:**

   ```bash
   git clone "https://github.com/reetjain01/live-tracker.git"
   cd live-tracker
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Start the server:**

   ```bash
   npm start
   ```

   The server will start on port 3000 by default.

4. **Open your browser and navigate to:**

   ```
   http://localhost:3000
   ```

## File Structure

```
project-root/
├── public/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── script.js
├── views/
│   └── index.ejs
├── app.js
└── package.json
```

- `public/css/style.css`: Styles for the application.
- `public/js/script.js`: JavaScript for handling geolocation and real-time updates.
- `views/index.ejs`: EJS template for rendering the map.
- `app.js`: Main server file for handling routes and WebSocket connections.
- `package.json`: Contains project dependencies and scripts.

## Usage

### Geolocation Tracking

- The application uses the browser's Geolocation API to track the user's location.
- The location is emitted to the server and broadcast to all connected clients.

### Real-time Map Updates

- The server broadcasts location updates to all clients.
- The map view and markers are updated dynamically based on the received location data.

## Troubleshooting

- **Error: `GET http://localhost:3000/socket.io/socket.io.js net::ERR_ABORTED 404 (Not Found)`**

  Ensure that the Socket.IO client script is included in the EJS template and that the server is running correctly.

- **Error: `Uncaught Error: Attempted to load an infinite number of tiles`**

  Ensure that the tile layer URL in Leaflet is correctly configured and does not result in infinite requests.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue if you have suggestions or improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
