# Installing

## Binary files

You can find binaries for your operating system at [releases page](https://github.com/majestrate/XD/releases).

Supported operating systems:

* GNU\Linux
* MacOS
* Windows
* FreeBSD

## Building from source

### Dependencies

* GNU Make
* GO 1.6 or higher


### Building

Right now the best way to build is with `make`:

    $ git clone https://github.com/majestrate/XD
    $ cd XD
    $ make

If you do not want to build with embedded webui instead run::

    $ make no-webui

You can build with go get using:

    $ go get -u -v github.com/majestrate/XD

Please note that using `go get` disables the webui.

#### Cross compile for Raspberry PI

Set `GOARCH` and `GOOS` when building with make:

    $ make GOARCH=arm GOOS=linux

