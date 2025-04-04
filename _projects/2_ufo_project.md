---
name: UFO Sightings Visualization
tools: [Python, Altair, Vega-Lite]
image: assets/pngs/ufo.png 
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

## View the Visualizations

<h4>📈 UFO Reports per Year (Interactive)</h4>
<iframe src="/assets/html/hw5_chart1.html" width="100%" height="550" frameborder="0"></iframe>

<h4>🗺️ UFO Sightings by State (Dropdown Select)</h4>
<iframe src="/assets/html/hw5_chart2.html" width="100%" height="550" frameborder="0"></iframe>

## The Data & Notebook

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/GeraintGui/GeraintGui.github.io/main/assets/data/ufo.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/GeraintGui/GeraintGui.github.io/blob/main/python_notebooks/ufo_visualization.ipynb" text="The Analysis" %}
</div>

