# A tilemap for Switzerland

This repository contains a square tilemap of the cantons and half-cantons of Switzerland. This is roughly based on ideas in http://blog.apps.npr.org/2015/05/11/hex-tile-maps.html and in http://aftertheflood.co/projects/london-squared-map.

## What you get
This repository contains everything you need to make these:

![Tilemap overlaid on geographically correct map](https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/Karte.png)
![Tilemap without the lakes](https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/Switzerland-Tiles%20-%20wo-Lakes.png)
![Result of the 1992 EEA vote in Switzerland](https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/Beispieldarstellung_Karte_EWR_Abstimmung.png)

## How to use
Please feel free to use all resources in this repository. The only thing to do: Please include a note saying "CC-BY EBP, www.ebp.ch". Thank you.

## Formats
* SVG
* Shapefile in CH1903 LV03 in the approximately correct location
* Example ArcGIS 10.3. project illustrating the use of the shapefile
* Some example graphics
* GeoJSON file, which can be viewed directly on GitHub. Conversion with `ogr2ogr`. Needs to be realigned for Mercator projection.

        ogr2ogr -f GeoJSON -s_srs epsg:21781 -t_srs crs:84 Switzerland_Tiles.geojson Switzerland_Tiles.shp


For more infos see: http://www.geo.ebp.ch/2016/01/07/tilemap-der-schweiz
