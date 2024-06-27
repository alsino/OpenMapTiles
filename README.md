# MapLibre GL JS Offline with Custom Vector Tiles

This is an example of hosting vector tiles with custom style and a local copy of MapLibre GL JS library on your own server.The MBTiles were downloaded for the city of Dortmund from MapTiler:

## Demo
https://alsino.github.io/OpenMapTiles/

# Download ready-made vector tiles from MapTiler:

- All OSM: https://data.maptiler.com/downloads/planet/
- Only Dortmund: https://data.maptiler.com/downloads/tileset/osm/europe/germany/dortmund/

# Host tiles without server in folder structure:

https://github.com/klokantech/vector-tiles-sample?tab=readme-ov-file#host-the-vector-tiles-without-any-server-at-all

# Turn tiles into folder structure:

mb-util --image_format=pbf dortmund.mbtiles dortmund
gzip -d -r -S .pbf \*
find . -type f -exec mv '{}' '{}'.pbf \;

# Example code (how to use with folder structure):

https://github.com/klokantech/mapbox-gl-js-offline-example/blob/gh-pages/index.html
