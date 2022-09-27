---
title: "Example: Embedding Altair & Hvplot Charts"
date: 2022-09-27
published: true
tags: [datavis, altair, hvplot, holoviews]
excerpt: "Embedding interactive charts on static pges using Jekyll."
altair-loader:
  altair-chart-1: "charts/measlesAltairWB.json"
hv-loader:
  hv-chart-1: ["charts/measlesHvplotWB.html", "500"]
toc: true
toc_sticky: true
---

## Altair Example

Below is a chart of the incidence of measles since 1928 for the 50 US states.

<div id="altair-chart-1"></div>

This was produced using Altair and embedded into this static web page. Note you can also display the Python code on this page:

```python
import altair as alt
alt.renders.enable('notebook')
```

## HvPlot Example

Lastly, the measles incidence produced using the HvPlot package:

<div id="hv-chart-1"></div>

## Notes

- See the [raw source code](http) of this post for details on how these charts were embedded.
- See the [lecture 13A slides](https://musa-550-fall-2021.github.io/slides/lecture-13A.html) for the code that produced these plots.

**Important, when embedding charts, you will likely need to adjust the width/height of the charts before embedding them in the page so they
fit nicely when embedded.
