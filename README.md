# docker-mariadb-percona

Docker setup for mariadb server with percona backup

This docker setup is based on https://hub.docker.com/_/mariadb/.

In addition to the options described in the manual above, this container offers hot backup
using percona backup and high memory configuration.


## Backup and restore

To backup, do this

    docker exec -i <container name> backup > backup_file.tar.bz2

To restore, do this:

    docker exec -i <container name> restore < restore_file.tar.bz2


## High memory configuration

To enable high memory configuration, add -e USE_HIGHMEM=1 when you run the container:

docker run -d -e USE_HIGHMEM=1 mariadb-percona


## Copyright and license

Copyright Nota 2015-2016, the Danish National Library for the Blind and Reading Impaired.

See LICENSE for license.


