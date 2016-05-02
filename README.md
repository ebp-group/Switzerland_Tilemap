# A tilemap for Switzerland

This repository contains a square tilemap of the cantons and half-cantons of Switzerland. This is roughly based on ideas in http://blog.apps.npr.org/2015/05/11/hex-tile-maps.html and in http://aftertheflood.co/projects/london-squared-map.

## What you get
This repository contains everything you need to make these:

####Tilemap overlaid on geographically correct map (&copy; swisstopo)
<img title="Tilemap overlaid on geographically correct map" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Comparison_geography.png" width="600">

####Tilemap (without lakes):
<img title="Tilemap (without lakes)" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Switzerland-Tiles%20-%20wo-Lakes.png" width="600">

####Example map 1: Result of the 1992 vote on accession to the EEA
<img title="Example map: Result of the 1992 vote on accession to the EEA" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Example_map_EEA_vote.png" width="600">

####Example map 2: Result of the 2016 vote on expulsion
<img title="Example map: Result of the 2016 vote on expulsion" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Example_map_Expulsion.jpg" width="600">

####Example map 3: Result of the 2016 vote on marriage taxation reform
<img title="Example map: Result of the 2016 vote on marriage taxation reform" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Example_map_Marriage_taxation_reform.jpg" width="600">

## How to use
Please feel free to use all resources in this repository. The only thing to do: Please include a note saying "Tilemap CC-BY [www.ebp.ch](http://geo.ebp.ch/2016/01/07/tilemap-der-schweiz)". Thank you.

## Formats
The [`data`](https://github.com/ernstbaslerpartner/Switzerland_Tilemap/tree/master/data) folder contains the following datasets and formats:

* GeoJSON file in Mercator ([EPSG:4326](http://spatialreference.org/ref/epsg/4326)) for use in web mapping
	* derived using: `ogr2ogr -f GeoJSON -s_srs epsg:3857 -t_srs crs:84 Switzerland_Tiles_EPSG4326_WGS1984.geojson Switzerland_Tiles_EPSG3857_WebMercator.shp` 
* Shapefile in Web Mercator ([EPSG:3857 / SR-ORG:7483](http://spatialreference.org/ref/sr-org/7483)) for use in web mapping frameworks such as [CartoDB](https://cartodb.com)
* Shapefile in CH1903 LV03 ([EPSG:21781](http://spatialreference.org/ref/epsg/21781/))
* Shapefile in CH1903+ LV95 ([EPSG:2056](http://spatialreference.org/ref/epsg/2056/))
* SVG file

Additional material:

* Example ArcGIS 10.3. project illustrating the use of the shapefiles
* Example graphics

For more infos see: http://www.geo.ebp.ch/2016/01/07/tilemap-der-schweiz (German) or http://www.ralphstraumann.ch/blog/2016/01/switzerland-tile-map (English).
