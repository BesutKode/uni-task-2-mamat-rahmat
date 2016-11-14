# Damar Island Open Data

This project aim to collect Open Data about Damar Island and visualize them.

<https://github.com/BesutKode/uni-task-2-mamat-rahmat>

## Collected Data and Script

There are some collected data, along with script to grab them from the sources and postprocess them sufficiently :

* Damar Island coastline data taken from [OpenStreetmap](https://www.openstreetmap.org/) using [Overpass API](http://overpass-api.de/). The license of the data is [Open Data Commons Open Database License (ODbL)](http://opendatacommons.org/licenses/odbl/).
* Damar Island mountain data taken from [OpenStreetmap](https://www.openstreetmap.org/) using [Overpass API](http://overpass-api.de/). The license of the data is [Open Data Commons Open Database License (ODbL)](http://opendatacommons.org/licenses/odbl/).
* Damar Island critical land taken from [Ministry of Forestry data repository](http://appgis.dephut.go.id/appgis/download.aspx). The license of the data is [Creative Commons Attribution Lisence (cc-by)](http://www.opendefinition.org/licenses/cc-by) which is stated in [data.go.id](http://data.go.id/dataset/data-lahan-kritis-di-maluku/resource/55ff4f8e-2db6-470e-80bd-d3a4e3d5b9e9).

The Script is written in NodeJS with some dependencies :

* request
* osmtogeojson
* togeojson
* xmldom

Generally the script duty is to grab data from source and convert them to GeoJson format for easy visualization.

## Visualization

Visualization is created with html page which use Bootstrap and OpenLayers. The demo page is located [here](https://besutkode.github.io/uni-task-2-mamat-rahmat/).

## Development

To reproduce the data grabing, make sure you had nodejs in your environtment. Install some dependencies with `npm install`, and run the script with `node script.js`.

To run web visualization, make sure that you had a webserver running for project root. You can use http-server node package as a simple web server is enough.

To add some data, you can add GeoJson data directly to project root (please make sure that the data is using Open Data Lisence), or add some code to the script to grab the data and postprocess them sufficiently.
