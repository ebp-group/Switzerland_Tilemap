# A tilemap for Switzerland

This repository contains a square tilemap of the cantons and half-cantons of Switzerland. This is roughly based on ideas in http://blog.apps.npr.org/2015/05/11/hex-tile-maps.html and in http://aftertheflood.co/projects/london-squared-map.

## What you get
This repository contains everything you need to make these:

#### Tilemap overlaid on geographically correct map (&copy; swisstopo)

<img title="Tilemap overlaid on geographically correct map" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Comparison_geography.png" width="600">

#### Tilemap (without lakes):

<img title="Tilemap (without lakes)" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Switzerland-Tiles%20-%20wo-Lakes.png" width="600">

#### Example map 1: Result of the 1992 vote on accession to the EEA

<img title="Example map: Result of the 1992 vote on accession to the EEA" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Example_map_EEA_vote.png" width="600">

#### Example map 2: Result of the 2016 vote on expulsion

<img title="Example map: Result of the 2016 vote on expulsion" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Example_map_Expulsion.jpg" width="600">

#### Example map 3: Result of the 2016 vote on marriage taxation reform

<img title="Example map: Result of the 2016 vote on marriage taxation reform" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/Example_map_Marriage_taxation_reform.jpg" width="600">

#### Example map 4: GitHub preview map of the Switzerland Tilemap GeoJSON file

[<img title="Example map: Sample map displaying the GeoJSON file" src="https://raw.githubusercontent.com/ernstbaslerpartner/Switzerland_Tilemap/master/examples/GitHub-GeoJSON-map.png" width="600">](https://github.com/ernstbaslerpartner/Switzerland_Tilemap/blob/master/data/Switzerland_Tiles_EPSG4326_WGS1984.geojson)

## How to use
Please feel free to use all resources in this repository. The only thing to do: Please include a note saying "Tilemap CC-BY [www.ebp.ch](http://geo.ebp.ch/2016/01/07/tilemap-der-schweiz)". Thank you.

## Formats
The [`data`](https://github.com/ernstbaslerpartner/Switzerland_Tilemap/tree/master/data) folder contains the data behind the tilemap in GeoJSON (geo-web-native), Shapefile (not great, but most broadly usable industry 'standard'), and SVG (web-native) formats. The tilemap depicting regularly spaced and gridded squares (and half-squares) the data should not generally be re-projected. E.g., the tilemap file in Swiss projection does show squares when drawn, e.g., in a GIS. But if you reproject it to WGS 1984 and look at it, the squares won't be squares anymore. Thus, every projection system available below is its own product, not simply a reprojection.

GeoJSON files are always in WGS 1984 ([EPSG:4326](http://spatialreference.org/ref/epsg/4326)), since that is what the standards require. However, the different GeoJSON files are made for displaying a regular (non-skewed, undistorted) tilemap in different spatial reference systems. The following files are available:

* **data for display in Web Mercator** ([EPSG:3857 / SR-ORG:7483](http://spatialreference.org/ref/sr-org/7483)) ...
  - **... as GeoJSON file** (WGS 1984, [EPSG:4326](http://spatialreference.org/ref/epsg/4326)), for use in web mapping frameworks
  - **... as Shapefile**, for use in web mapping frameworks such as [**CartoDB**](https://cartodb.com)
* **data for display in Natural Earth Projection** ([cf.](https://pro.arcgis.com/en/pro-app/latest/help/mapping/properties/natural-earth.htm)) ...
  - **... as GeoJSON file** (WGS 1984, [EPSG:4326](http://spatialreference.org/ref/epsg/4326)). Use this file in e.g. [**Datawrapper**](https://www.datawrapper.de) and choose "Natural Earth" projection for the tiles to display as regularly spaced squares.
  - **... as Shapefile**, for use in desktop GIS or web mapping frameworks with custom projections
* **data for display in CH1903+ LV95** ([EPSG:2056](http://spatialreference.org/ref/epsg/2056/)) **as Shapefile**, for use in desktop GIS or web mapping frameworks with custom projections
* **data for display in CH1903 LV03** ([EPSG:21781](http://spatialreference.org/ref/epsg/21781/), a deprecated spatial reference system) **as Shapefile**, for use in desktop GIS or web mapping frameworks with custom projections
* **data as SVG file**

Additional material:

* Example ArcGIS 10.3+ project illustrating the use of the shapefiles
* Example graphics

For more infos see: http://www.geo.ebp.ch/2016/01/07/tilemap-der-schweiz (German) or http://www.ralphstraumann.ch/blog/2016/01/switzerland-tile-map (English).
