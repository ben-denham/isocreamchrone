# Isocreamchrone

**View the map of travel times to vaccination centres here:
https://htmlpreview.github.io/?https://github.com/ben-denham/isocreamchrone/blob/master/jupyter/notebooks/isocreamchrone.html**

Isocreamchrone is a tool for creating isochrone maps that show how
long it would take to get from any point on a map to one of a set of
locations. Applied to map the travel time to the nearest Covid-19
vaccination centre in New Zealand. Based on the [GraphHopper isochrone
API](https://www.graphhopper.com/blog/2018/09/17/graphhopper-routing-engine-0-11-release-open-sourcing-the-isochrone-module/),
inspired by
https://thespinoff.co.nz/society/11-10-2021/travel-times-to-every-suburbs-closest-vaccination-centre-on-one-interactive-map/.

## Usage

* Install dependencies:
  * [Docker Community Edition](https://docs.docker.com/get-docker/) (>= 17.09)
  * [Docker Compose](https://docs.docker.com/compose/install/) (>=
    1.17) (Included with Docker Desktop on Mac/Windows)
* Download map files into `data/`:
  * `new-zealand-latest.osm.pbf` from
    https://download.geofabrik.de/australia-oceania/new-zealand.html
  * `nz-coastlines-and-islands-polygons-topo-150k.shp` from
    https://data.linz.govt.nz/layer/51153-nz-coastlines-and-islands-polygons-topo-150k/
* Run `docker-compose up`
* Open `http://localhost:8080/notebooks/isocreamchrone.ipynb` in your browser
* Run the notebook to generate the isochrone map.
