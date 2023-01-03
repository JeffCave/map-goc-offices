# Mapping the locations of Government of Canada offices

The goal of this project is to create a simple, user-friendly map that displays the locations of all Government of Canada (GoC) offices, based on the [Directory of Federal Real Property (DFRP)](https://www.tbs-sct.gc.ca/dfrp-rbif/home-accueil-eng.aspx), and also including [GCcoworking spaces](https://www.canada.ca/en/public-services-procurement/news/2019/06/gccoworking-new-flexible-alternative-workplaces-for-government-of-canada-employees.html). 

With the announcement of the [common hybrid work model for the Federal Public Service](https://www.canada.ca/en/government/publicservice/staffing/common-hybrid-work-model-federal-public-service.html), some public servants may be interested in examining the possibility of working from alternative workplaces within 125 km of their location, whether it be other GoC offices and/or GCcoworking locations.


## How to use the map

[Opening the map](map_government_offices.html) will display all GoC offices as small blue circles. Hovering over any of the offices will make a box appear with the name of the site, its street address, municipality and province/territory.

Similar to Google Maps, you can use the scroll wheel on your mouse to zoom in and out on the map. You can hold down the left mouse button to drag the map. In the top-right corner, you can choose between displaying all GoC offices and displaying only GCcoworking locations.

You can also select your location on the map with a left mouse click, and a circle of radius 125 km will be drawn around that marker. Any small blue circles within the larger circle are within 125 km of the selected location. Another left mouse click will update your selected location marker and the surrounding circle.

[Another version of the map](map_labels.html) is the same as above, with the exclusion of the location selection and surrounding circle.


## Caveats

This map only includes properties that are located in Canada, and that have latitude/longitude coordinates in the DFRP.

The 125 km is a distance "as the crow flies"; it's not based on a road network distance. So depending on the road density in your area, this may only serve as a rough approximation.

While the circle of radius 125 km will encapsulate all GoC offices within it, that does not mean that all (or any) of those offices are necessarily available as a work location for any given public servant. This would depend on the nature and departmental occupancy of each office, as well as its seating availability. Unfortunately, this information does not appear to be contained in the DFRP data. If you know of a data source that contains such information, please contact me (see the "Notes and credits" section below).


## Running the code

If you want to run this code yourself, you can download the repository, as well as installing [R](https://www.r-project.org/) and [RStudio](https://posit.co/products/open-source/rstudio/).

The data subfolder contains the DFRP data for GoC offices as of 2023-01-01. The R code file explains the steps needed to update the data.


## Notes and credits

If you want to provide feedback, you can find my work e-mail on GEDS. I currently work at NRCan. (I'm not including it directly here because of the existence of spam-focused e-mail scrapers.)

While I am working as a public servant as of the time of this writing, this project was developed and released solely on my own time and in my capacity as a private individual. It has no affiliation with the GoC, and I hold no public opinions on the common hybrid work model for the Federal Public Service.

This project was built using R and [Leaflet](https://leafletjs.com/). The R code file includes commented links to online resources (mainly Stack Overflow) where I was able to resolve analogous issues I encountered during development. Thanks to all of those awesome people.

Thank you to Reddit user graciejack who [described the appropriate search criteria](https://old.reddit.com/r/CanadaPublicServants/comments/zso3hz/ottawa_offices_in_the_east_end/) for the DFRP.
