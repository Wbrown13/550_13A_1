---
title: "Shreveport Supermarket Accessibility Analysis"
date: 2022-10-25
published: true
tags: [datavis, hvplot, holoviews]
excerpt: "Preliminary analysis of 'food deserts' using Google Maps API and Open Street Map data."
hv-loader:
  hv-chart-1: ["charts/shv_food_desert.html", "610"]
toc: true
toc_sticky: true
---

This map depicts which areas of Shreveport have easiest driving access to supermarkets (shown as red dots). The colored circles represent nodes in Shreveport's road network. Yellow areas are within close driving distances (less than a mile) of supermarkets, while residents neighborhoods shaded green or blue will have to drive farther to buy groceries. 

Use the map tools to hover over individual supermarkets (and view their information), or zoom in and examine individual neighborhoods. 

Supermarket information was queried from the Google Maps API, while the road network was created in Pandana and the visualization made with the Bokeh plotting library using Holoviz. All analysis was done with Python in a Jupyter Notebook.

Future iterations could improve the analysis by querying Google Maps at multiple locations around Shreveport with smaller search radii to ensure all supermarkets are included.

<div id="hv-chart-1"></div>
