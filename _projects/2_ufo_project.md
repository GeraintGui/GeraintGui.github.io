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

Figure 1 shows the number of UFO sightings and sighting reports reported each year. I wanted Figure 1 to show not only “When did people report the most UFOs?” but also “What did they say in that year?” Each point on the line represents a specific year, and the y-axis shows the total number of reports. I have set up the display below Figure 1 to show the top 20 original sighting reports. To create this graph, I grouped the dataset by year and used Pandas to count the number of reports per year. The chart uses line graph markers with dots to emphasize the yearly values, so no additional use of color was needed in my opinion. x-axis encodes the year as an ordinal value, and y-axis encodes the count as a quantitative field. Interactivity is demonstrated by the fact that when the user clicks on any of the year dots, a data table appears below the chart showing up to 20 UFO reports for the selected year. 

Figure 2 is different from Figure 1 in that I used a spatial narrative to tally the total number of UFO sightings reported by each state in the United States. This is because the map can show the geographic context that is not well explained by the bars. This visualization is static and does not include interactions beyond hovering. I used Altair's mark_geoshape() projection albersUsa to render state boundaries from TopoJSON files. The counts for each state use the color blue, where darker blue indicates more sightings. Color encoding is quantitative. I also added tools to display state FIPS IDs and total counts on mouse hover. The reason for displaying FIPS codes instead of state names or abbreviations is because the underlying TopoJSON map uses its FIPS numeric code. to ensure an accurate data join using Altair's transform_lookup(), I mapped each state's abbreviation to its corresponding FIPS code. For the data conversion, I grouped the UFO dataset by STATE and counted the number of reports for each state. I combined the stats with the ids in TopoJSON, allowing the Altair chart to be colored for each state based on its total number of sightings.




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

