# Final Project - Command Line GIS Fall 2025
# Mutiara Indah Puspita Sari 

## Interactive Map: Lava Hazard Zone & School Accessibility

<iframe src="school_lavahazard.html" height="550" width="100%"></iframe>

## Map 1: 15-minute School Access from Lava Hazard Zones 1-2

<iframe src="map1.png" height="900" width="100%"></iframe>

## Map 2: Population Density with Lava Hazard Zones 1-2

<iframe src="map2.png" height="970" width="100%"></iframe>

## Description

A short description of the datasets you used to create your maps, that answers the following questions (and anything else you want to say about your topic).

This project is a thematical research regarding volcanoes. I use Hawaii County only since it has one of the most active volcanoes in USA and I found that they have an interesting map of lava hazard zones. Using the required data & methods needed (Census, spatial join/geoprocessing), I make two static maps: 1) 15-minute School Access from Lava Hazard Zones 1-2 and 2) Population Density with Lava Hazard Zones 1-2. For the interactive map, i do an interactive map of Lava Hazard Zone & School Accessibility with 2 basemaps, tooltips of lava hazard zones that have information of layer when hovered, and popups that redirect to the school sites.

- Where did you find them?
I extensively search around the datasets that Hawaii County (the big island) have of volcanoes. Class suggested i use shelter maps, I did not find a good location of it officially. I did find a list of them unofficial, somewhere, where I could not really find again. But since it is just a matter of data, school dataset that I found is also a strategic one since school (usually they have big fields), can be used as a temporary shelters. Hospital locations are too few to use, I am afraid I wont have any result.
  
- Who prepared them? How recently were they updated?
  - ACS 5 years for population density (people/km^2) at the block group level, that shows unreliable data with CV ≥ 40.
  - Lava hazard zones (1-9) from USGS. I treat zone 1-2 as the most important piece in this research. https://geoportal.hawaii.gov/datasets/volcano-lava-flow-hazard-zones update: June 1, 2024 at 11:19:47 AM GMT+7
  - USA Volcano. https://www.ncei.noaa.gov/access/metadata/landing-page/bin/iso?id=gov.noaa.ngdc.mgg.hazards:G02135 
  - Schools, geocoded from Hawaii Dept of Edu's excel sheet. https://hawaiipublicschools.org/enrolling-in-school/find-your-school/. Possibly data set is same since September, 2021, this info from the school district area shp in hawaii
  - Network from OSM. Tracked the 15 minutes travel time from lava hazard zones 1-2 as suggested by class. I believe this is an open source with people updating it, so probably updated daily.
  
- What format were they originally in? Did you have to do anything to make them mappable (table join, spatial join, geocoding, aggregation, etc.)?
  1. Map 1: 15-minute School Access from Lava Hazard Zones 1-2
     - geoprocessing = clip road network of hawaii county
     - spatial overlay = school inside 15 mins of zone 1-2
     - geocoded schools from excel address
  2. Map 2: Population Density with Lava Hazard Zones 1-2
    - calculate popden & search unreliable data with high CV more than 40
    - geoprocessing = reprojection
  3. Interactive Map: Lava Hazard Zone & School Accessibility
    - layer control, basemaps, popups
    - heatmaps
  
- Were there any issues with data quality that you had to address?
  - Not at all
  
