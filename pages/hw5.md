layout: page
title: "HW5 - Interactive Visualizations"
permalink: /hw5/

Visualization 1: UFO Reports Per Year

This visualization shows the number of reported UFO sightings over time.I used a line chart with year on the x-axis and report count on the y-axis. Each point is interactive via tooltip.Data was cleaned by parsing the datetime column and extracting the year with pd.to_datetime.The line makes it easy to spot increases in reporting behavior, especially after 1990.👉 Click a year on the chart to view the actual UFO reports below.This helps users connect trends with real observations.

Visualization 2: UFO Reports by State (Choropleth Map)

This map shows total UFO report counts per U.S. state.I used a geoshape mark with Albers USA projection and colored states by number of reports using a blue color scale.Data was grouped by state, mapped to FIPS codes, and merged with a TopoJSON file of U.S. state boundaries.This map was built completely in Altair using Vega-Lite’s topo_feature + transform_lookup.

Interactivity

The first chart includes interactive selection: when you click on any year, a table below updates to show the first 20 UFO reports from that year, including shape, city, and comments.This allows the viewer to go beyond just trends and explore actual content. The second chart is static.