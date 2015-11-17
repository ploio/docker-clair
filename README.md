# Portefaix Clair

* Master :
[![Circle CI](https://circleci.com/gh/portefaix/docker-clair/tree/master.svg?style=svg)](https://circleci.com/gh/portefaix/docker-clair/tree/master)

* Develop :
[![Circle CI](https://circleci.com/gh/portefaix/docker-clair/tree/develop.svg?style=svg)](https://circleci.com/gh/portefaix/docker-clair/tree/develop)


![logo](http://pkgs.alpinelinux.org/assets/alpinelinux-logo.svg)

[Alpine Linux][] is a Linux distribution built around musl libc and BusyBox.
This image is based on the official Alpine Linux.

[Clair][] is a container vulnerability analysis service from [CoreOS][]

Port exported are : `6060` and `6061`

Volumes exported are : `db`.

## Usage

    $ docker run --rm=true -it -p 6060:6060 -p 6061:6061 -v /tmp:/db portefaix/clair \
    	/clair --db-type=bolt --db-path=/db/portefaix.db

## Supported tags

- `0.0.1` [![](https://badge.imagelayers.io/portefaix/clair:0.0.1.svg)](https://imagelayers.io/?images=portefaix/clair:0.0.1 'imagelayers.io')


## License

See [LICENSE](LICENSE) for the complete license.


## Changelog

A [ChangeLog.md](ChangeLog.md) is available.


## Contact

Nicolas Lamirault <nicolas.lamirault@gmail.com>


[Alpine Linux]: http://www.alpinelinux.org

[Clair]: https://github.com/coreos/clair
[CoreOS]: https://coreos.com
