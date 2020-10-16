<html>

<head>
  <title>Studio Week 2: Submission through a github page. </title>
  <!-- Adding in the Leaflet CSS file -->
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.6.0/dist/leaflet.css" />
  <!-- Adding Leaflet JavaScript file -->
  <script src="https://unpkg.com/leaflet@1.6.0/dist/leaflet.js"></script>
  <!-- Adding styling info for the map -->
  <style type="text/css">
    /* Add a CSS rule that selects an element with the ID "mapId" and gives it a height of 600 pixels */
    #mapId {
     height: 600px;
   }
	body {
  background-color: #FADF98;
}
 ul {
  background: #FCF3CF;
  padding: 10px;
}
  </style>
  <!-- Adding styling info for page layout by reading in a CSS file -->
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <h1 style="font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif">Studio Week 2 <br> Raster tiles with Leaflet submitted by Arpita Shalini.</h1>
  <!-- Add multiple pages to web page-->
  <!-- active class displays the grey box around current page-->
  <ul>
    <li><a class="active" href="index.html" target="_self" style="color: #09166c">Output 1</a></li>
    <li><a href="Mapbox-gl-js-cwm.html" target="_self" style="color: #8ebf42">Output 2</a></li>
    <li><a href="Mapbox-gl-js-ct.html" target="_self" style="color: #56596b">Output 3</a></li>
    <li><a href="Mapbox-gl-js-bm.html" target="_self" style="color: #8ebf42">Output 4</a></li>
  </ul>
  <br>

  <!-- Add a div with id="mapId" to give the map somewhere to go -->
  <div id="mapId"></div>
  <script>
    // Create a variable called "map" to house your Leaflet map and all of its functionality
    var map = L.map('mapId').setView([37.754700, -122.420790], 14);
    /* 
     * Use Leaflet's tileLayer method to create a new tile layer, then add it to the map 
     ** Reference: https://leafletjs.com/reference-1.6.0.html#tilelayer
     */
     L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
     attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
   }).addTo(map);

    /* Try changing out the tile source for something else. Hint: you can find 
     * lots of tile sources here: https://leaflet-extras.github.io/leaflet-providers/preview/ 
     */ 
     L.tileLayer('https://{s}.tile.openstreetmap.fr/hot/{z}/{x}/{y}.png', {
	maxZoom: 19,
	attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors, Tiles style by <a href="https://www.hotosm.org/" target="_blank">Humanitarian OpenStreetMap Team</a> hosted by <a href="https://openstreetmap.fr/" target="_blank">OpenStreetMap France</a>'
}).addTo(map);


  </script>
</body>

</html>
