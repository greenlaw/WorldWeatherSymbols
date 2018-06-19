WorldWeatherSymbols
===================

A complete set of WMO weather symbols in SVG ~~with full metadata~~ that will work with [GeoServer](http://geoserver.org/).

This repository was forked from https://github.com/OGCMetOceanDWG/WorldWeatherSymbols because the original symbols can't be imported by GeoTools/GeoServer (latest versions tested were GeoServer 2.12-SNAPSHOT 7eb5a4f238bfd643fcc3504975a3e69f2dfaa158 / GeoTools 18-SNAPSHOT df098b50341ddeb293299a1d7e1c96cde2c3235a).  

The compatibility issue appears to be that GeoTools is having problem with the custom namespaces, e.g. ```<svg:svg>``` where ```<svg>``` was expected. The simplest fix was to remove the custom ```xmlns``` attributes and corresponding element prefixes. The metadata elements were also removed entirely.

At some point I hope to submit a pull request to GeoTools to address the real issue, but this is the quick-and-dirty fix.

I claim no ownership or copyright over this content - [OGCMetOceanDWG](https://github.com/OGCMetOceanDWG) deserves all the credit for their work to create these symbols.

Download
--------

The full repository sources are available at https://github.com/greenlaw/WorldWeatherSymbols.git

Accessing the symbols
---------------------

### Pre-generated PNGs

A set of pre-generated PNGs are available for download at https://github.com/OGCMetOceanDWG/WorldWeatherSymbols/releases/download/0.6.0/WorldWeatherSymbols-0.6.0-png.zip.

### Building PNGs

To build PNG equivalents of the symbols, run ```./scripts/wws_manage.sh png```.  Output PNG files are located in ```png/```.  [Inkscape](https://inkscape.org) is required to run the conversions.  

Viewing the symbols
---------------------

### The symbols and their descriptions

A list of symbols with their filenames and associated descriptions is provided in [symbols subfolders](https://github.com/greenlaw/WorldWeatherSymbols/tree/master/symbols/) in the respective README.md files ([example for the Ft_Fronts subfolder](https://github.com/greenlaw/WorldWeatherSymbols/tree/master/symbols/Ft_Fronts/)). Those README.md files are generated automatically by the [wws_manage.sh](https://github.com/greenlaw/WorldWeatherSymbols/tree/master/scripts/wws_manage.sh) script. These lists act a short guides to the WMO WorldWeatherSymbols.


### Displaying the symbols on GitHub

WorldWeatherSymbols can be displayed directly on Github either by opening the symbol's svg file or by using [RawGit](https://rawgit.com/) to include symbols in Markdown-formatted files, example: ![Front_Cold_at_surface](https://cdn.rawgit.com/greenlaw/WorldWeatherSymbols/master/symbols/Ft_Fronts/WeatherSymbol_WMO_Front_Quasi-stationary_at_surface.svg).

Version history
---------------------

See [HISTORY.txt](https://github.com/greenlaw/WorldWeatherSymbols/tree/master/HISTORY.txt)
