# Mapping Earthquakes
## Overview 

In my role as a data visualization specialist for the Disaster Reporting Network, a non-profit company that provides data-driven storytelling on disasters around the world, I have been asked to build insightful data visualizations with interactive features on earthquakes from around the world. The head of the earthquake disaster response team believes that this project will be useful for his team which includes reporters and data visualization specialists. He hopes that making earthquake maps informative and easy to use on desktop and mobile phones will generate positive vibes about the disaster reporting network. In my role, I will be supporting website and mobile application developments by using the latest URL for GeoJSON earthquake data from the US Geological Survey website. I will traverse and retrieve geographical coordinates and the magnitudes of earthquakes for the last seven days using JavaScript and the D3.js library. I will then use the Leaflet library to plot the data on a Mapbox map through an API request and create interactivity for the earthquake data.
 
On the map, the magnitude and location of each earthquake will be shown in a pop-up marker. The diameter of the markers for each earthquake will reflect the magnitude of the earthquake in their size and color. Earthquakes with higher magnitudes will appear larger and darker in color with a legend providing the context for the map data.
To illustrate the relationship between the location and frequency of seismic activity and Tectonic plates I will add font lines on the map.

## Results 
The earthquake GeoJSON data was retrieved using the code;
``` JavaScript
d3.json("https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_week.geojson").then(function(data)
```

The center of our map is the geographic center of the United States with coordinates [39.5, -98.5], and default layer streets. Aside the streets layer, The outdoors and satelliteStreets map styles were also added to the map. 
We assign a tileLayer method to a variable 'streets"
The earthquake data has the geometry object type Point. 

A style was assigned to each earthquake by using a circle marker and adjusting the line color, fill color, opacity, fill opacity, stroke, weight, and radius.

The radius represents the earthquake's magnitude.Earthquakes with a magnitude of 0 were plotted with a radius of 1 and all other magnitudes were plotted by multiplying by 4. The earthquake circle markers were also color-coded based on magnitude.The magnitudes and locations were also added as popups for each earthquake.


The earthquake data was added as an overlay on both the Streets and Satellite tile layers so that the data can be turned on and off by the viewer. A legend was also added for the color range of the earthquakes.

The earthquake data in relation to the tectonic plates’ location on the earth was shown on the map. Also, all earthquakes with a magnitude greater than 4.5 were shown on the map.

A second and third overlay were added to the map for the tectonic plate data and major earthquake data respecivly. 
The tectonic plate data and major earthquake data are added to the overlay object

the three datasets can be toggled on or off

The tectonic plate data is added as a second layer group 

The tectonic plate data is added to the overlay object

The two earthquake data and tectonic plate data are displayed on the map when the page loads

## Summary
