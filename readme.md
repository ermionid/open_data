# Open (geo)data IRCEL-CELINE
License: https://creativecommons.org/licenses/by/4.0/

## Catalog Service for the Web (`CSW`)
Metadata is hosted via:
* http://geo.irceline.be/csw (under construction)

Documentation specific CSW implementation:
* http://geonetwork-opensource.org/manuals/trunk/eng/users/index.html

General documentation of the OGC standard for `CSW`:
* http://www.opengeospatial.org/standards/cat

## Web Map Service (`WMS`) - viewing service
A WMS serves geo-registered map images

Our end-point:
* http://geo.irceline.be/wms

See `GetCapabilities`:
* http://geo.irceline.be/wms?service=wms&version=1.3.0&request=GetCapabilities

The following workspaces serve a subsection of the data:
1. http://geo.irceline.be/rio/wms
    - interpolated maps of RIO 4x4km
    - Coverage Belgium and per region
    - see further [details here](dataset/rio.md)
2. http://geo.irceline.be/realtime/wms
    - measurement data per station
    - selection possible via time parameter
    - see further [details here](dataset/measurements.md)
3. http://geo.irceline.be/annual/wms

### Encodings
Available encodings (see [format](http://docs.geoserver.org/latest/en/user/services/wms/outputformats.html#wms-output-formats) parameter):
* png
* png8
* jpeg
* tiff

See full list in [GetCapabilities](http://geo.irceline.be/wms?service=wms&version=1.3.0&request=GetCapabilities) under `<GetMap>` `<Format>`

### Projections
Available projections (see [srs](http://docs.geoserver.org/latest/en/user/services/wms/reference.html#wms-getmap) parameter):
* EPSG:31370
* EPSG:4258
* EPSG:4326
* EPSG:900913

### Documentation WMS
Documentation interacting with the specific WMS implementation:
* http://docs.geoserver.org/latest/en/user/services/wms/reference.html

General documentation of the OGC standard for `WMS`:
* http://www.opengeospatial.org/standards/wms

## Web Feature Service (`WFS`) - download service
A WFS serves vector format geographical data.

Our end-point:
* http://geo.irceline.be/wfs

See `GetCapabilities`:
http://geo.irceline.be/wfs?service=wfs&version=2.0.0&request=GetCapabilities

### Encodings
Available encodings (see [format](http://docs.geoserver.org/latest/en/user/services/wms/outputformats.html#wms-output-formats) parameter):
* gml
* json
* csv
* kml
* shp
* js

See full list in [GetCapabilities](http://geo.irceline.be/wfs?service=wfs&version=2.0.0&request=GetCapabilities) under `<ows:Parameter name="outputFormat">`

### Projections
Most commonly used projections are supported (cf [EPSG](https://www.epsg-registry.org/))

### Documentation WFS
Documentation specific `WFS` implementation:
* http://docs.geoserver.org/latest/en/user/services/wfs/reference.html

General documentation of the OGC standard for `WFS`:
* http://www.opengeospatial.org/standards/wfs

## Sensor Observation Service (SOS) - download service
A SOS serves sensor data (time series, metadata of stations and measuring devices) collected at a specific geographical location.

Our end-point:
* http://geo.irceline.be/sos

Browse data via the following clients:
* http://viewer.irceline.be
### SOAP
Client:
http://geo.irceline.be/sos/client

Documentation specific `SOS` implementation:
https://wiki.52north.org/bin/view/SensorWeb/SensorObservationServiceIVDocumentation

SOS adapted for e-reporting under the Air Quality Directive:
https://wiki.52north.org/bin/view/SensorWeb/AqdEReporting

General documentation of the OGC standard for SOS:
* http://www.opengeospatial.org/standards/sos

### REST-api
* http://geo.irceline.be/sos/api/v1/

Documentation:
* http://geo.irceline.be/sos/static/doc/api-doc/

## Legends
See: https://github.com/irceline/map_legends

## Abbreviations
A list of abbreviations used in het layer names:

| Abbreviation | Description                                                                                      |
|:-------------|:-------------------------------------------------------------------------------------------------|
| hmean        | hourly mean (timstamp = end-time of hour)                                                        |
| 24hmean      | 24 hour running mean (timstamp = end-time of 24 hour period)                                     |
| 8hmean       | 8 hour running mean (timstamp = end-time of 8 hour period)                                       |
| dmean        | mean concentration during one day (hmean 01h00 to 24h00 - timstamp = 01h00 of the following day) |
| anmean       | mean concentration during one calendar year                                                      |
| rio          | RIO interpolation - see [rio dataset](dataset/rio.md)                                            |
| station      | data measured in a measuring station                                                             |
| vl           | the network "Flanders"                                                                           |
| wl           | the network "Wallonia"                                                                           |
| br           | the network "Brussels"                                                                           |
