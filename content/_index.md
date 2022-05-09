---
title: "Biking in the Big Apple"

description: "One step closer to green New York."
# 1. To ensure Netlify triggers a build on our exampleSite instrance, we need to change a file in the exampleSite directory.
theme_version: '2.8.2'
cascade:
  featured_image: 'media/new-york-bg.jpg'
---
Freshly arrived in Copenhagen, when getting out of the bus, I almost got ran over... by a bike. Since that initial shock of the amount of bikes and their omnipresence, I grew accustomed to the biking culture here in Denmark. Only half a year after moving here, I don't know a person that doesn't own a bike, and according to a study from 2016, **41%** of Copenhagen's inhabitants commute to work or school by bike. Danes are serious about climate change, and biking is a big part of implementing that green mindset.

More and more big cities such as London follow suit, trying to reduce the carbon footprint by encouraging this ecological form of transportation. However, some of them are falling behind. It came as a surprise that the Big Apple was so small in the biking department - only **1.1%** of New Yorkers cycle to work! But if there's one thing New York is good at is providing access to the data about the city. So let's dive into cycling data to try to give them a push towards being green. 






### Sources

1. [Cycling in Dublin and Copenhagen](https://www.researchgate.net/publication/331134372_The_Current_State_of_Cycling_Infrastructure_in_Dublin_and_Copenhagen_A_Comparison_of_Cycling_Infrastructure_in_8_Radial_Routes_into_the_City_Centre_of_Dublin_and_Copenhagen)
2. [Cycle commuters in London double](https://www.bikes.org.uk/cycle-commuters-in-london-double/)
3. [Denmark wants to be a frontrunner in fight against climate change](https://environment.yale.edu/news/article/why-denmark-wants-to-be-a-frontrunner-in-fight-against-climate-change)
4. [US Census - biking to work in big cities](https://www.census.gov/library/stories/2019/05/younger-workers-in-cities-more-likely-to-bike-to-work.html?fbclid=IwAR0xwhffS35MmPUmMU3zgLntV4lG0LLP1s-OXlGNe62ZGvmdefbM40R2hv0 )








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