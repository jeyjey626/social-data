---
title: "Biking in the Big Apple"

description: "One step closer to green New York."
# 1. To ensure Netlify triggers a build on our exampleSite instrance, we need to change a file in the exampleSite directory.
theme_version: '2.8.2'
cascade:
  featured_image: 'media/new-york-bg.jpg'
---
Welcome to my blog with some of my work in progress. I've been working on this book idea. You can read some of the chapters below.

This is an example of placing folium/html maps:
1. Upload the .html file to static/html.
2. reference folium shortcode passing string "html/yourmap.html" as argument - just like below!
3. Profit

![Calendar plot](/png/plot_route_distribution.png)

![Calendar plot](/png/plot_dayofweek_distribution.png)

![Calendar plot](/png/plot_calendar.png)

{{<folium "html/nyc_map.html">}}

{{<folium "html/nyc_map2.html">}}

{{<folium "html/nyc_map3.html">}}

{{<folium "html/nyc_map4.html">}}