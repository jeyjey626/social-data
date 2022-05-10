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

## The route of the problem

The first thing we should look at is how much of New York is accessible by bike, and what conditions do cyclists face. The city's bike routes are classified by varying degree of safety, where only protected and standard paths separate you from traffic.
According to the article on [smartasset](https://smartasset.com/data-studies/most-bike-friendly-cities-2021) we know that about **124** miles of protected lanes exist in New York City, compared to around **8,000** miles of streets.

The city's bike routes are classified by varying degree of safety, and counting the number of segments of each type can be seen here:

![Route type distribution](/svg/plot_route_distribution.svg)

It shows that there is a large amount of standard bikes, separated from vehicles with paint. However, the runner-up for most segments are *"sharrows"* - where a bike shares the lane with cars. It's not necessarily a bad thing, even though less safe, it still signals that cyclists are expected there. 

Great, we know the routes. But what about our cyclists? Let's attempt to gain some insight on why do they bike by looking at the distribution of citybike bike trips over the week.

![Bike trips by day of week](/svg/plot_dayofweek_distribution.svg)

CitiBike is a bike sharing service. With that in mind, the fact that the most trips are performed during weekdays could mean that they are the people we're after - commuters. To further corroborate that let's plot a more complex graph on that data - a calendar graph.
![Calendar plot](/svg/plot_calendar.svg)

Looking at this gradient, we can see that mot trips are recorded between the morning rush hours - 6 and 9. It is worth noting, that we suspect that around 7am the server system or database may have maintenance time, as it is very unlikely for that specific rush hour to be so empty across the whole year. But even with that break, we can now with more confidence say, that this data should give us insights about New York's commuters.

## Navigating the city jungle

Let's learn even more about New Yorkers and see where they commute. This is the top 100 all time most popular bike trips with CitiBike until 2017. Each trip is presented as a line connecting two station dots.

{{<folium "html/nyc_map.html">}}

The vast majority of bike traffic is located in Manhattan, with only few popular routes in Brooklyn and Queens. The most attended spots are Hudson river's bank, Grand Central Terminal, Chelsea and the Brooklyn bridge. A few trips can be found in Central Park, although we reckon they might be relax-driven, similarly to trips to the river's bank. Southern Manhattan is overflowing with skyscrapers and offices, so these trip seem to likely be commute.

Though Manhattan seems to be rich in bike routes, when taking a closer look, you can still see some popular journeys that can be impeded by inconveniently located infrastructure. For example, let's get from the Grand Central Terminal to the 23rd Street - it's right down the road! However, we're following bike lanes, so one would have to first arrive at the 6th Avenue and spend most of the trip on that road, in order to get safely to the desired CitiBike station. That adds 3 blocks of biking perpendicularly to the destination instead towards it! 

Those were the all-time favorites, but let's drill down and see where do they drive each month between 2014 and 2017.

{{<folium "html/nyc_map2.html">}}

Warmer seasons favor leisure trips - Central Park, Brooklyn Bridge and Hudson's bank are among the most frequented.  During winter, Grand Central Terminal and the Penn Station are the top destinations. The scenario we believe is likely is office workers taking the train to Manhattan and then grabbing a bike to get to work.

Near the Grand Central Terminal there are only a few bike paths heading south, the closest one located on the 6th Avenue. In Brooklyn and Queens most people travel following the bike routes, and there are not that many further into these districts. There are still quite a few spots, especially near the Graham Avenue, where no cycle paths are present.

Now let's create another time-based map but for the days of the week.

{{<folium "html/nyc_map4.html">}}

In the map 01 indicates monday and 07 sunday. We can see that for the weekdays, the lines steadily emerge from the the Grand Central Terminal And New York Penn Station areas to the nearby streets. This changes drastically for saturday and sunday, where again we can se most of the trips are being made to the aforementioned leisure locations - Hudson river bank and the Central Park. For Brooklyn and Queens the trips are mostly located near the East River bank during the work week. It could suggest that offices are also located there and people commute to work. The opposite is spotted for the Brooklyn Bridge - most of the popular trips there are during the weekend.


Up until now, we were mostly focusing on the whole bike trips, but now let’s dig into the CitiBike stations. The company has over **1500** stations in New York. Let’s see where they are located and which ones are used the most.

{{<folium "html/nyc_map3.html">}}

As expected, Manhattan is a district with the highest number of stations. However, there is still a significant number of stations in Brooklyn and Queens. Now spots lacking bike routes clearly stand out. The stations are located in almost every street in Manhattan, some of them not adjacent to any bike lane. It's especially prominent south of the  Grand Central Terminal, which is unfortunate as it is a big commuting hub. We observe that in Brooklyn as well - examples being Nostrand Avenue and Fulton Street.

## Equal biking

## Destination: Green Apple

### Sources

1. [Cycling in Dublin and Copenhagen](https://www.researchgate.net/publication/F331134372_The_Current_State_of_Cycling_Infrastructure_in_Dublin_and_Copenhagen_A_Comparison_of_Cycling_Infrastructure_in_8_Radial_Routes_into_the_City_Centre_of_Dublin_and_Copenhagen)
2. [Cycle commuters in London double](https://www.bikes.org.uk/cycle-commuters-in-london-double/)
3. [Denmark wants to be a frontrunner in fight against climate change](https://environment.yale.edu/news/article/why-denmark-wants-to-be-a-frontrunner-in-fight-against-climate-change)
4. [US Census - biking to work in big cities](https://www.census.gov/library/stories/2019/05/younger-workers-in-cities-more-likely-to-bike-to-work.html?fbclid=IwAR0xwhffS35MmPUmMU3zgLntV4lG0LLP1s-OXlGNe62ZGvmdefbM40R2hv0 )
5. [Protected bike lanes in NYC](https://smartasset.com/data-studies/most-bike-friendly-cities-2021)
6. [Miles of streets in NYC](https://www.cityandstateny.com/politics/2020/04/how-nyc-will-close-up-to-100-miles-of-streets-to-cars/176073/)
7. [Types of bike lanes in New York](https://parkingtickets.org/traffic-rules-and-regulations/nyc-bike-lanes/)







This is an example of placing folium/html maps:
1. Upload the .html file to static/html.
2. reference folium shortcode passing string "html/yourmap.html" as argument - just like below!
3. Profit


{{<folium "html/nyc_map.html">}}

{{<folium "html/nyc_map2.html">}}

{{<folium "html/nyc_map3.html">}}

{{<folium "html/nyc_map4.html">}}