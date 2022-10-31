---
title: "Identifying Shreveport Heat Islands with Landsat Imagery"
date: 2022-10-25
published: true
tags: [datavis, hvplot, holoviews]
excerpt: "A test in embedding charts on web pages with Jekyll."
hv-loader:
  hv-chart-1: ["charts/shv_mean_surface_temp.html", "600"]
  hv-chart-2: ["charts/shv_hotspots.html", "500"]
  hv-chart-3: ["charts/shv_redlining.html", "500"]
  hv-chart-4: ["charts/shv_heat_islands.html", "500"]
toc: true
toc_sticky: true
---

Located in the middle of the Sun Belt, Shreveport is famous for its hot, sticky summers. But on a searing September day, some parts of town are verifiably hotter than others. This series of maps uses Landsat imagery to examine which neighborhoods have the highest average surface temperatures.

The map below gives us a first look at an image collected by the Landsat 8 satellite on September 3, 2019, a day when air temperatures in Shreveport peaked around 100 degrees. This image already has gone through some processing: we calculated the Normalized Difference Vegetation Index (NDVI) and combined it with the image's thermal infrared data to apply atmospheric corrections and transformations needed to reveal land surface temperature. 

Here we can already start to make out Shreveport's major hotspots, such as the regional airport. Meanwhile rural areas and suburbs are much cooler. You can hover over the map to view the actual temperatures (they are noted as 'value' in the tooltip box). 

<div id="hv-chart-1"></div>

The next map uses the same data from the map above, but only displays areas where surface temperatures exceed 90 degrees. Here the city's hotspots show up much more clearly - in addition to the regional airport, we can see that surface temperatures are quite high in downtown Shreveport, the shopping strip at Youree Drive, and various industrial areas around town. This patterns mirror urban 'heat island' effects found in cities around the country, where a lack of vegetation and large amounts of paved areas and big, dark building roofs soak up heat and warm the areas around them. 

<div id="hv-chart-2"></div>

The next pair of maps examine Shreveport's heat islands in the context of redlining, the New Deal-era practice in which cities' neighborhoods were divided into categories of supposed investment risk, but often isolated minority neighborhoods and denied their residents much-needed loans, with consequences extending to the present day. 

The map below shows the historic boundaries of Shreveport's redlining districts:
* Green - Class A ("Best")
* Blue - Class B ("Still desirable")
* Yellow - Class C ("Declining")
* Red - Class D ("Hazardous")

<div id="hv-chart-3"></div>

This map blends the redlining map with the earlier surface temperature data, showing the average surface temperature in each redlining district. Do Class A neighborhoods look warmer or cooler than less desirable areas?

<div id="hv-chart-4"></div>

On average, Shreveport's Class A neighborhoods indeed tend to run at least 1 degree cooler than other parts of town (with Class B areas on average being the warmest):

* Class A    86.2 degrees
* Class C    87.4 degrees
* Class D    87.7 degrees
* Class B    89.0 degrees

Class A neighborhoods are able to keep a little cooler thanks to larger amounts of street trees and other vegetation, and are less likely to be close to industrial parks whose large paved areas and warehouse/factory buildings help to soak up heat. 
