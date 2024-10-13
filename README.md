Mapbox GL JS Project: Guides
Overview
This project utilizes Mapbox GL JS to display an interactive map that shows stops between Sulur and Ukkadam. The map is initialized with a button that, when clicked, animates a marker along predefined coordinates.

Features
Interactive map display using Mapbox GL JS.
Animated marker movement between specified coordinates.
Responsive design for various screen sizes.
Prerequisites
A Mapbox account to obtain an access token.
Basic knowledge of HTML, CSS, and JavaScript.
Setup Instructions
Clone the Repository


git clone <repository-url>
cd <repository-directory>
Open the HTML File
Open the index.html file in your preferred web browser.

Obtain a Mapbox Access Token

Sign up or log in to your Mapbox account.
Navigate to the Access Tokens section and create a new token if you don't have one.
Replace the placeholder access token in the script with your own:

const map = new mapboxgl.Map({
    container: 'map',
    style: 'mapbox://styles/mapbox/streets-v9',
    zoom: 12,
    center: [77.108824, 11.023618]
});

const marker2 = new mapboxgl.Marker();

function btn() {
    setInterval(move, 1000);
}

function move() {
    marker2.setLngLat([left[value], right[value]]).addTo(map);
    value++;
}
mapboxgl.accessToken = 'YOUR_MAPBOX_ACCESS_TOKEN';
Usage
Click the Show stops between Sulur to Ukkadam button to start the animation of the marker moving along the specified coordinates.
The map is centered around the coordinates [77.108824, 11.023618] with a zoom level of 12.
Code Structure
HTML: The main structure of the webpage, including the map container and button.
CSS: Basic styling for the map and button positioning.
JavaScript: Initializes the Mapbox map, sets up the marker, and handles the button click event to animate the marker.
License
This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgments
Mapbox GL JS Documentation
Thanks to the Mapbox team for providing the tools to create interactive maps.
