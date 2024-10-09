# Tiles

The location to store tiles

## Table Of Contents

* [Package Description](#packagedescription)
    * [Tile Format](#tile-format)
    * [Package File Example](#package-file-example)

## Package Description

This file contains the description for the latest version.  It contains the following fields:

name

> This should be a descriptive name of the set

version

> This should match a version file in the current directory

date

> This should be the date of the upload.

tiles

> This is a list of described tiles in the tile format

### Tile Format

The tile format is structured with the following fields:

alt

> The text equivalent of the tile to be displayed.  This will be used incase of a loading error client side

src

> The source file name

targets

> The number of targets to request.  0 will not display any targets.  If there are not enough players to be selected, then the tile will be skipped.

### Package File Example

```
0.1.example.json
{
    "name": "The Lookout Drinking Game",
    "version": "1.0.0",
    "date": "10/09/2024",
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