
# mkgmap style for OSM hiking maps

[Style rules][1] and [TYP definitions][2] for making a
hiking map from [OpenStreetMap](http://www.openstreetmap.org/) data
for a [Garmin GPS][3] using [mkgmap][4].
The cartography is mainly adopted from [OpenTopoMap][5].

This project currently only offers a style, you have to render your maps on your own.
If you are interested in pre-rendered maps, let me know it.

Note that the style is under heavy development, so you want to wait if you plan to use the style for productivity.
A map preview follows as soon as the style is developed further.

# How to render a map
The following steps describe how to get a Garmin map from OSM data using this style definition.

## Fetching the data
You need to download OSM data somehow.
This can be done by several methods, including [download servers][6] or direct download from the [OSM page][7].

## Rendering the map
Build the TYP file from `OpenHikingMap.txt` with [mkgmap][4] by using (expecting the parent directory as working directory):

	mkgmap OpenHikingMap.txt

Then build the map file using mkgmap:

	mkgmap -c OpenHikingMap/arguments --style-file=OpenHikingMap OpenHikingMap.typ all/osm/data/*.osm

For large areas you'll need to use a splitter.

Licensed under [CC-BY-NC-SA][8].

[1]: http://wiki.openstreetmap.org/wiki/Mkgmap/help/style_rules
[2]: http://wiki.openstreetmap.org/wiki/Mkgmap/help/TYP_files
[3]: http://www.garmin.com/us/products/onthetrail
[4]: http://www.mkgmap.org.uk/
[5]: https://www.opentopomap.org/
[6]: https://download.geofabrik.de/
[7]: https://www.openstreetmap.org/export
[8]: https://creativecommons.org/licenses/by-nc-sa/4.0/
