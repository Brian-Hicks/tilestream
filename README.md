TileStream
----------
A high performance tile server and simple web viewer for [MBTiles][1] files.

[1]:[http://mbtiles.org]


Features
--------
- MBTiles-based tile server
- Minimal gallery view and OpenLayers based viewer of tiles
- Support for MBTiles interaction using [Wax](http://github.com/mapbox/wax)


Requirements
------------
- *TileStream client*
  - Tested: Chrome 6+, Firefox 3+, IE8+
  - May work: Opera 11
- *TileStream server*
  - Tested: Mac OS X 10.6, Ubuntu 10.10
  - At least 613MB memory
  - May work: Older versions, other POSIX-compliant systems
  - The [prerequisites for node][2] (python, libssl-dev)

[2]:https://github.com/ry/node/wiki/Installation


Installation: Mac OS X 10.6
---------------------------
Install [Xcode][3] for Mac OS X.

Download and unpack TileStream. Build & install:

    git clone -b master-ndistro git://github.com/mapbox/tilestream.git
    cd tilestream
    ./ndistro

Start TileStream:

    bin/tilestream

TileStream should now be accessible from a browser at `http://localhost:8888`.

[3]:http://developer.apple.com/technologies/tools/xcode.html


Installation: Ubuntu 10.10
--------------------------
Install build requirements:

    sudo apt-get install build-essential libssl-dev libsqlite3-0 libsqlite3-dev

Download and unpack TileStream. Build & install:

    git clone -b master-ndistro git://github.com/mapbox/tilestream.git
    cd tilestream
    ./ndistro

Start TileStream:

    PATH=bin tilestream

TileStream should now be accessible from a browser at `http://localhost:8888`.


Usage
-----
MBTiles files should be placed in the `tiles` directory. Each
tileset can be previewed at `http://localhost:8888/tileset/[filename]` where
`[filename]` is the name of the tileset file without the `.mbtiles` extension.

Commandline options:

    Usage: tilestream [COMMAND] [OPTION]
    Commands:
      start
        start server
        --config=PATH      Pass options via JSON config file at PATH.
        --uiPort=PORT      UI server port. Defaults to 8888.
        --uiHost=HOST      UI server hostname. Defaults to localhost.
        --tilePort=PORT    Tile server port. Defaults to 8888.
        --tileHost=HOST    Tile server hostname(s). Defaults to localhost.
        --tiles=PATH       Path to tiles directory.


Tests
-----
You can run the TileStream tests using expresso:

    PATH=bin expresso modules/tilestream/test/tilestream.test.js


Contributors
------------
- [Young Hahn](http://github.com/yhahn)
- [Tom MacWright](http://github.com/tmcw)
- [Will White](http://github.com/willwhite)
- [Konstantin Käfer](http://github.com/kkaefer)
- [Dane Springmeyer](http://github.com/springmeyer)
