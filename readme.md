
# mkgmap style for OSM hiking maps

[Style rules][1] and [TYP definitions][2] for making a
hiking map from [OpenStreetMap](http://www.openstreetmap.org/) data
for a [Garmin GPS][3] using [mkgmap][4].
The cartography is mainly adopted from [OpenTopoMap][12].

This project currently only offers a style, you have to render your maps on your own.
If you are interested in pre-rendered maps, let me know it.

Note that the style is under heavy development, so you want to wait if you plan to use the style for productivity.
A map preview follows as soon as the style is developed further.

# How to render a map
The following steps describe how to get a Garmin map from OSM data using this style definition.

## Fetching the data
You need to download OSM data somehow.
This can be done by several methods, including [download servers][10] or direct download from the [OSM page][11].

## Rendering the map
Build the TYP file from `hiking_typdef.txt` with [mkgmap][4] by using (expecting the parent directory as working directory):

	mkgmap hiking_typdef.txt

Then build the map file using mkgmap:

	mkgmap -c OpenHikingMap/arguments --style-file=OpenHikingMap hiking_typdef.typ all/osm/data/*.osm

For large areas you'll need to use a splitter.

Licensed under [CC BY][9].

[1]: http://wiki.openstreetmap.org/wiki/Mkgmap/help/style_rules
[2]: http://wiki.openstreetmap.org/wiki/Mkgmap/help/TYP_files
[3]: http://www.garmin.com/us/products/onthetrail
[4]: http://www.mkgmap.org.uk/
[5]: http://www.kartverket.no/globalassets/standard/bransjestandarder-utover-sosi/symbol.pdf
  "Symbolfonter for friluftsliv og sport (1997). Statens kartverk Landkartdivisjonen, ISBN 82-90408-52-8"
[6]: http://www.cgpsmapper.com/
[8]: http://no.wikipedia.org/wiki/Marka_(Oslo)
[9]: http://creativecommons.org/licenses/by/4.0/
[10]: https://download.geofabrik.de/
[11]: https://www.openstreetmap.org/export
[12]: https://www.opentopomap.org/
