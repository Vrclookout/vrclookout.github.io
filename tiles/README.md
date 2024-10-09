# Tiles

The location to store tiles

## Table Of Contents

* [package.json](#packagejson)
* [Version Files](#version-files)
    * [Version File Example](#version-file-example)
* [Tile Format](#tile-format)

## package.json

This file contains the description for the latest version.  It contains the following fields:

name

> This should be a descriptive name of the set

latestVersion

> This should match a version file in the current directory

date

> This should be the date of the upload.


## Version Files

This is a `JSON` string that will be used to describe available tiles.  It contains the following fields:

basePath

> This is a relative path from this directory

tiles

> This is a list of described tiles in the tile format

### Version File Example

```
0.1.example.json
{
    "basePath": "src/",
    "tiles": [
        {
            "alt": "I'm the first tile",
            "src": "first_tile.png",
            "targets": 0
        },
        {
            "alt": "I'm the second tile with a request for two targets",
            "src": "second_tile.png",
            "targets": 2
        }
    ]
}
```

## Tile Format

The tile format is structured with the following fields:

alt

> The text equivalent of the tile to be displayed.  This will be used incase of a loading error client side

src

> The source file name

targets

> The number of targets to request.  0 will not display any targets.  If there are not enough players to be selected, then the tile will be skipped.