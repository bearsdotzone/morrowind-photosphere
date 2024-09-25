# OpenMW

[You can take a spherical photo in OpenMW, works best in 0.45](https://gitlab.com/OpenMW/openmw/-/issues/7720)

Put `screenshot type = spherical 10000 5000 4096` in your settings.cfg under [Video] (maxes out at 10k pixels, vertical must be 1/2 for photo-sphere-viewer)

# ImageMagick

To create the streaming tiles from the larger image:

`convert test046.png -crop 16x8@ tiles/tile-%01d.png`

[Needs to be a power of 2 number of tiles](https://photo-sphere-viewer.js.org/guide/adapters/equirectangular-tiles.html)

To create the low-res initial image:

`convert test046.png -resize 12.5% test046-small.png`

Remember to adjust the tileUrl function if you change the number of tiles


# Web Server for Testing
`npx http-server`
