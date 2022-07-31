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

The streets and satelliteStreets map styles were used on the map. 
We assign a tileLayer method to a variable 'streets"
The earthquake data has the geometry object type Point. 



## Summary
