# My Travel Map

Below is an interactive map of all the places I've visited.

<div id="map-container" style="position: relative; width: 100%; height: 600px; overflow: hidden;">
   <div id="map" style="height: 100%; width: 100%;"></div>
</div>

<script src="https://unpkg.com/leaflet@1.9.3/dist/leaflet.js"></script>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.3/dist/leaflet.css" />

<script>
    // Initialize the map and set its view
    var map = L.map('map').setView([20, 0], 2);  // Centered on the world with zoom level 2

    // Add a base layer (OpenStreetMap tiles)
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    }).addTo(map);

    // Add markers for places you've visited
    var places = [
        { lat: 48.8566, lon: 2.3522, name: 'Paris, France' },
        { lat: 40.7128, lon: -74.0060, name: 'New York, USA' },
        { lat: 35.6895, lon: 139.6917, name: 'Tokyo, Japan' }
    ];

    places.forEach(function(place) {
        L.marker([place.lat, place.lon])
            .addTo(map)
            .bindPopup(place.name);
    });
</script>
