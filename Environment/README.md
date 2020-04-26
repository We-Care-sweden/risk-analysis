# We Care Sweden
`Devpost Submission Link` : https://devpost.com/software/wecare-5l9dgi
[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)
![](https://github.com/We-Care-sweden/risk-analysis/issues/3#issue-606941275)

### EUvsVirus Hackathon
Environmental Risk and Heatmap Development using PyKrige Kriging modelling method
  - This section contains raw datasets for Kriging model development
  - Dataset variables (x,y,z) will consist of  **LONGITUDE** (x), **LATITUDE**  (y) and **HOTSPOT** (z) to generate  2D interpolation and visualisation of live hotspots in Sweden based on user-input postal codes.
  - Datum used for all **LAT** (x) and **LONG** (y) is **WGS 84 EPSG:3857 Pseudo-Mercator** (Same datum as Google Maps and Bing Maps)

### Tech

WeCare team thanks a number of open source projecs as part of building this solution

* [PyKrige](http:/https://github.com/GeoStat-Framework/PyKrige/blob/master/README.rst/ "PyKrige") - 2D and 3D Ordinary and Universal Kriging
* [Open Refine](http:/https://openrefine.org/ "Open Refine") - Powerful tool for working with messy data
* [Geo Stats Models](http:/https://github.com/cjohnson318/geostatsmodels/ "Geo Stats Models") - Implementation of ideas from Clayton V. Deutsch and Michael Pyrcz's book Geostatistical Reservoir Modeling
* [Geostatpy](http:/https://github.com/exepulveda/geostatpy/ "Geostatpy") -  Geostatistical python toolbox.
* [Institute of Earth Sciences Coders](http:/https://iescoders.com/plotting-the-geospatial-data-clipped-by-coastlines-in-python/ "Institute of Earth Sciences Coders") -  Plotting the geospatial data clipped by coastlines in Python by Utpal Rai
* [Svenska Städer](http:/https://github.com/sphrak/svenska-stader/ "Svenska Städer") -  Swedish cities in csv format with coordinates 
* [Svenska Städer](http:/https://github.com/sphrak/svenska-stader/ "Svenska Städer") -  Swedish cities in csv format with coordinates 
* [Open Geocoding API](http:/https://developer.mapquest.com/documentation/open/geocoding-api/address/get/ "Open Geocoding API") - Geocoding service enables you to take an address and get the associated latitude and longitude.
* [Google Maps Platform](http:/https://developers.google.com/maps/documentation/geocoding/intro/ "Open Geocoding API") -  Geocoding API web service
* [Folkhälsomyndigheten](https://experience.arcgis.com/experience/09f821667ce64bf7be6f9f87457ed9aa) - Sweden COVID19 dataset
* [Statistikdatabasen](http://www.statistikdatabasen.scb.se/pxweb/en/ssd/) - Sweden population and location statistics
* [Simple Maps](http:/https://simplemaps.com/data/se-citiesd/) - Sweden population and location statistics
* [Diva GIS](http:/https://www.diva-gis.org/gdata/) - Global GIS Shapefiles 


### Datasets

This repository includes main source files to compute Environmental impacts. 

- [`city_stat`](./city_stat.ipynb) should be re-executed every hour to get the most updated number of "death", "infected", and "intensive_care" per city, to update [city_stat.csv](./city_stat.csv). Data will be fetched from [Folkhälsomyndigheten](https://experience.arcgis.com/experience/09f821667ce64bf7be6f9f87457ed9aa).

- [municipality_stat.csv](./municipality_stat.csv) includes risk factors per municipality in greater Stockholm area. 

- [population_municipality.csv](population_municipality.csv) and [population_county.csv](population_county.csv) inlcude updated number or residents in various municipalities and counties in Sweden, obtained from [Statistikdatabasen](http://www.statistikdatabasen.scb.se/pxweb/en/ssd/), and reformatted in our data frame using [`population_to_csv`](population_to_csv.ipynb) script.
- County-and-municipality-and-area-codes focuses on deriving area codes of Sweden counties and municipalities (Statistiska centralbyrån)
- Get_swe_geocoding.ipynb script obtains the geocoding API along with the necessary **LON** and **LAT** locations for (x,y) data. This produces swe_geocoding.csv
- population_to_csv.ipynb script focuses on compiling total area codes and municipalities data, and geolocation into .csv format

License
----

Creative Commons
