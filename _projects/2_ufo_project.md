---
name: UFO Sightings Visualization
tools: [Python, Altair, Vega-Lite]

description: An interactive analysis of UFO reports over time and across states.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

## Overview

This project uses Altair (via Vega-Lite) to explore patterns in UFO sighting reports from a cleaned public dataset.  
It includes two visualizations:  
📈 A time series line chart that lets users click a year to see actual reports.  
🗺️ A choropleth map showing UFO sightings by U.S. state.

## View the Visualization

👉 [**Click here to view the full project**](/hw5/)

## The Data & Notebook

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/GeraintGui/GeraintGui.github.io/main/data/ufo.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/GeraintGui/GeraintGui.github.io/blob/main/python_notebooks/ufo_visualization.ipynb" text="The Analysis" %}
</div>
