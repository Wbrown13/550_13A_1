---
title: "New Orleans Neighborhood Data Viewer"
date: 2023-03-17
published: true
tags: [datavis, hvplot, holoviews]
excerpt: "A tour of an online application that takes user input, queries a database, and return charts and maps on specific New Orleans neighborhoods."
toc: true
toc_sticky: true
---
## Introduction

This article shows snippets a dynamic web page with a custom front and backend. The page accepts user inputs to select a neighborhood in New Orleans, queries an online database, and returns a series of charts and maps showing where that neighborhood compares to others in a variety of metrics. 

The API is built using Python Flask, and relies on a PostgreSQL/PostGIS database that I built and maintain on an Amazon Web Services (AWS) Relational Database Service (RDS). Data in the database is sourced from [New Orleans open data portal](https://datadriven.nola.gov/home/), the US Census, and other sources.

While I have taken the website offline to save hosting costs, the animated gifs below demonstrate how it works.

## User Input Page

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/images/input_to_landing.gif)

Website visitors have the option of selecting a neighborhood from a dropdown menu or typing in a New Orleans address or place name in the text box. Here the user enters "Cafe Du Monde". After clicking submit, the Flask app uses Mapbox to determine that Cafe Du Monde is in the Vieux Carre neighborhood (also known as the French Quarter). 

(If no address is provided or the address cannot be found in New Orleans, the user will be notified and the Vieux Carre neigbhorhood will be shown by default).

## General Charts and Maps

The results page shows charts and maps that place the selected neighborhood in the wider New Orleans context for a variety of metrics related to demographics, amenities, transportation, and more. 

Charts and maps are made in the Bokeh plotting library using Holoviews. 

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/images/landing_tour_hover.gif)

All visualizations are interactive and can be hovered over to view custom tooltips. 

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/images/landing_tour_zoom.gif)

The toolbar at the right of the map can be used to pan and zoom the map by scrolling and drawing a box to zoom.

## Detailed Charts and Maps

While the main page focuses on showing how the selected neigbhorhood stacks up against others, most metrics have a 'drill down' button that takes visitors to a separate page with more detailed information. 

![alt-text]({{ site.url }}{{ site.baseurl }}/assets/images/drill_down.gif)

In this example, the user clicks through to see a more detailed map of hotels and short-term rental (STR) properties in the Vieux Carre neighborhood. Clicking through tells the Flask app to perform an intersection analysis of the citywide hotels data table with PostGIS, ensuring that only hotels in the chosen neigbhorhood are displayed.
