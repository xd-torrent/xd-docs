## Requirements

XD uses Invisible Internet Protocol (I2P) for anonymizing and encrypting connections.
Thus it **requires user to run I2P router with SAM bridge enabled**.

[i2pd](http://i2pd.website) has SAM bridge enabled by default and is recommended, [Java implementation](https://geti2p.net) will work too.

## Getting started with XD

Once you have built or obtained a release, a webui will be enabled by default at http://127.0.0.1:1488/ .

Windows users are encouraged to use the webui if they can't use the command line tool.

## Command Line (unix)

To autogenerate a new config and start:

    $ ./XD torrents.ini

After started put torrent files into `./storage/downloads/` to start downloading.

To seed torrents put data files into `./storage/downloads/` first then add torrent files.

If you compiled with web ui it will be up at http://127.0.0.1:1488/ .

To use the command line tool you must symlink the `XD` binary to `XD-cli`:

    $ ln -s XD XD-cli

Adding torrents from seed file over i2p:

    XD-cli add http://somesite.i2p/some/url/to/a/torrent.torrent

Listing active torrents:

    XD-cli list

To increase how many pieces to request in parallel use `set-piece-window` command (may be removed in future):

    XD-cli set-piece-window 10

## Command Line (windows)

On Windows: make a copy of the file called `XD-cli.exe`.

All commands are done in the same manner as in unix, except `/` needs escaping depending on what terminal in use.

TODO: add more docs for windows.

