# building the daemon #


## requirements ##

* linux or freebsd
* libsodium 1.0 or higher
* imagemagick
* ffmpeg
* sox

## supported go versions ##

* `go 1.6` or higher with redis driver

* `go 1.3` or higher without redis driver

## debian ##

Get `go 1.6` from [here](https://golang.org/dl/) for your platform

Get the dependancies

    sudo apt-get update
    sudo apt-get --no-install-recommends install imagemagick libsodium-dev ffmpeg sox build-essential git ca-certificates

*Note: ffmpeg is likely no longer in your default repos, add [deb-multimedia] (http://www.deb-multimedia.org/) or build it from [source] (https://www.ffmpeg.org/releases/)*

Check out the repo and build it

    git clone https://github.com/majestrate/nntpchan
    cd nntpchan
    ./build.sh

If you want to build without supporting redis then build with the `--no-redis` flag

    ./build.sh --no-redis
    
Setup your [database](database.md)

To configure nntpchan eiter run `./srndv2 setup` and browse to http://127.0.0.1:18000 to use the wizard or edit srnd.ini [by hand](srnd.ini.md).
