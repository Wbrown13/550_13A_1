---
title: "Shreveport Neighborhood Housing Market in the Pandemic"
date: 2022-10-24
published: true
tags: [datavis, hvplot, holoviews]
excerpt: "A test in embedding charts on web pages with Jekyll."
hv-loader:
  hv-chart-1: ["charts/shv_zillow_line1.html", "500"]
  hv-chart-2: ["charts/shv_zillow_line2.html", "500"]
  hv-chart-3: ["charts/shv_zillow_line3.html", "500"]
  hv-chart-4: ["charts/shv_zillow_heatmap.html", "500"]
toc: true
toc_sticky: true
---

A recent article identified Shreveport as one of the cities left behind in the pandemic-era house price boom. The specific reasons lie beyond the scope of this article but likely relate to Shreveport's long-standing challenges including demographic decline, lack of investment, perceived poor job opportunities, and more.

I wanted to take a quick look at neighborhood-level house price data from Zillow to see if Shreveport's housing market sluggishness was widespread or concentrated in certain areas. 

The line chart below supports the latter scenario, with a clear divergence in neighborhood-level performance since the start of the pandemic. Specifically, Shreveport's rich neighborhoods are getting richer (high and sharply rising house prices) while its poor ones are getting poorer (low and stagnant/falling house prices). Mouse hover or press on a line to identify the neighborhood. 

<div id="hv-chart-2"></div>

I know the above chart is a little messy with eighteen lines. You can view each neighborhood's price trend individually using the dropdown menu in the chart below.

<div id="hv-chart-1"></div>

The next chart shows the cumulative percentage change in home prices for each neighborhood since January 2020. The difference between winners and losers is stark, with a clear cluster of neighborhoods whose prices have risen by 10-20% or more, while others have been close to flat or even fallen precipitously. 

<div id="hv-chart-3"></div>

This heatmap shows the same cumulative change data, but hopefully makes the diverging performances easier to read than the (admittedly messy) line chart. 

<div id="hv-chart-4"></div>
