# Mapping Earthquakes
## Overview 

In my role as a data visualization specialist for the Disaster Reporting Network, a non-profit company that provides data-driven storytelling on disasters around the world, I have been asked to build insightful data visualizations with interactive features on earthquakes from around the world. The head of the earthquake disaster response team believes that this project will be useful for his team which includes reporters and data visualization specialists. He hopes that making earthquake maps informative and easy to use on desktop and mobile phones will generate positive vibes about the disaster reporting network. In my role, I will be supporting website and mobile application developments by using the latest URL for GeoJSON earthquake data from the US Geological Survey website. I will traverse and retrieve geographical coordinates and the magnitudes of earthquakes for the last seven days using JavaScript and the D3.js library. I will then use the Leaflet library to plot the data on a Mapbox map through an API request and create interactivity for the earthquake data.

## Results 

The earthquake GeoJSON data which has the geometry object type Point was retrieved using the code:

``` JavaScript
d3.json("https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_week.geojson").then(function(data))

```

The center of the map is the geographic center of the United States with coordinates [39.5, -98.5], and default layer streets. Aside the streets layer, the outdoors and satelliteStreets map styles were also added to the map so that the three datasets can be toggled on or off by the viewer. A base layer was created to hold all three maps using the code;

``` JavaScript
// Create a base layer that holds all three maps.
let baseMaps = {
  "Streets": streets,
  "Satellite": satelliteStreets,
  "Outdoors": outdoors
};

```

A style was assigned to each earthquake by using a circle marker and adjusting the line color, fill color, opacity, fill opacity, stroke, weight, and radius. The diameter of the markers for each earthquake reflects the magnitude of the earthquake in size and color. Earthquakes with a magnitude of 0 were plotted with a radius of 1 and all other magnitudes were plotted by multiplying by 4. The earthquake circle markers are also color-coded based on magnitude. Earthquakes with higher magnitudes appear darker in color. The magnitudes and locations of each earthquake were also added as pop-up markers.

The earthquake data in relation to the tectonic plates’ location on the earth was added as a second layer group. To illustrate this relationship between the location and frequency of seismic activity and tectonic plates, font lines were added on the map. Also, all earthquakes with a magnitude greater than 4.5 were shown on a separate map. A second and third overlay were added to the map for the tectonic plate data and major earthquake data respecivly. 
 
## Summary
When the webpage loads, the two earthquake data and tectonic plate data are displayed on the map. The default map displayed when the page loads is as shown:

![image](https://github.com/GerlechJen/Mapping_Earthquakes/blob/main/Images/default%20map.png)

----

**Completed by:** Jennifer Anno-Kusi

**Email:** jannokusi@gmail.com 

