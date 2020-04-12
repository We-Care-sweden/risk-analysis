This repository includes main source files to compute Environmental impacts. 

- [`city_stat`](./city_stat.ipynb) should be re-executed every hour to get the most updated number of "death", "infected", and "intensive_care" per city, to update [city_stat.csv](./city_stat.csv). Data will be fetched from [Folkhälsomyndigheten](https://experience.arcgis.com/experience/09f821667ce64bf7be6f9f87457ed9aa).

- [municipality_stat.csv](./municipality_stat.csv) includes risk factors per municipality in greater Stockholm area. 

- [population_municipality.csv](population_municipality.csv) and [population_county.csv](population_county.csv) inlcude updated number or residents in various municipalities and counties in Sweden, obtained from [Statistikdatabasen](http://www.statistikdatabasen.scb.se/pxweb/en/ssd/), and reformatted in our data frame using [`population_to_csv`](population_to_csv.ipynb) script.
