# GoKoala

## Introduction 

For features, GoKoala implements Parts 1, 2 and 5. GoKoala also implements other OGC API modules.

GoKoala is built as a cloud native implementation. With respect to OGC API Tiles, Styles, GeoVolumes the goal is to keep a narrow focus, meaning complex logic is delegated to other implementations. For example, vector tile hosting may be delegated to a vector tile engine, 3D tile hosting to object storage, raster map hosting to a WMS server, etc.

This application is deliberately not multi-tenant, it exposes an OGC API for one dataset. Want to host multiple datasets? Spin up a separate instance/container.

See [this list of API's](https://api.pdok.nl/) for a list of APIs that implement the OGC API using GoKoala

See [GoKoala documentation for an up to date list of features](https://github.com/PDOK/gokoala?tab=readme-ov-file#features)

## HTML landing page:

The following examples are performed on the [Administrative boundaries](https://api.pdok.nl/kadaster/bestuurlijkegebieden/ogc/v1) OGC API.

## Example queries

* See what the server implements:
[https://api.pdok.nl/kadaster/bestuurlijkegebieden/ogc/v1/conformance](https://api.pdok.nl/kadaster/bestuurlijkegebieden/ogc/v1/conformance)

* Get the list of collection metadata:
[https://api.pdok.nl/kadaster/bestuurlijkegebieden/ogc/v1/collections/gemeentegebied?f=json](https://api.pdok.nl/kadaster/bestuurlijkegebieden/ogc/v1/collections/gemeentegebied?f=json)

* Request the features in another CRS (3857):
[https://api.pdok.nl/kadaster/bestuurlijkegebieden/ogc/v1/collections/gemeentegebied/items?crs=http://www.opengis.net/def/crs/EPSG/0/3857&f=json](https://api.pdok.nl/kadaster/bestuurlijkegebieden/ogc/v1/collections/gemeentegebied/items?crs=http://www.opengis.net/def/crs/EPSG/0/3857&f=json)
