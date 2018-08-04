# Docker-based WordPress Stack

[![Build Status](https://travis-ci.org/anaxexp/wordpress4docker.svg?branch=master)](https://travis-ci.org/anaxexp/wordpress4docker)

## Introduction

WordPress4Docker is a set of docker images optimized for WordPress. Use docker-compose.yml file from this repository to spin up a local environment for WordPress on Linux, macOS and Windows. 

* Read the docs on [**how to use**](https://docs.anaxexp.com/stacks/wordpress/local#usage)
* Follow [us on Twitter](https://twitter.com/anaxexphq) to track future updates
* Join [community slack](https://slack.anaxexp.com) to ask questions

## Stack

The WordPress stack consist of the following containers:

| Container     | Versions           | Service name    | Image                              | Default |
| ------------- | ------------------ | ------------    | ---------------------------------- | ------- |
| [Nginx]       | 1.15, 1.14, 1.13   | `nginx`         | [anaxexp/wordpress-nginx]            | ✓       |
| [Apache]      | 2.4                | `apache`        | [anaxexp/php-apache]                 |         |
| [WordPress]   | 4                  | `php`           | [anaxexp/wordpress]                  | ✓       |
| [PHP]         | 7.x, 5.6           | `php`           | [anaxexp/wordpress-php]              |         |
| [MariaDB]     | 10.3, 10.2, 10.1   | `mariadb`       | [anaxexp/mariadb]                    | ✓       |
| [PostgreSQL]  | 10, 9.x            | `postgres`      | [anaxexp/postgres]                   |         |
| [Redis]       | 4.0, 3.2           | `redis`         | [anaxexp/redis]                      |         |
| [Varnish]     | 4.1                | `varnish`       | [anaxexp/wordpress-varnish]          |         |
| [Node.js]     | 9.11, 8.11, 6.14   | `node`          | [anaxexp/node]                       |         |
| [Solr]        | 7.x, 6.6, 5.5      | `solr`          | [anaxexp/solr]                       |         |
| Elasticsearch | 6.x, 5.6, 5.5, 5.4 | `elasticsearch` | [anaxexp/elasticsearch]              |         |
| Kibana        | 6.x, 5.6, 5.5, 5.4 | `kibana`        | [anaxexp/kibana]                     |         |
| [Memcached]   | 1.5                | `memcached`     | [anaxexp/memcached]                  |         |
| [AthenaPDF]   | 2.10.0             | `athenapdf`     | [arachnysdocker/athenapdf-service] |         |
| [Webgrind]    | 1.5                | `webgrind`      | [anaxexp/webgrind]                   |         |
| [Blackfire]   | latest             | `blackfire`     | [blackfire/blackfire]              |         |
| [Mailhog]     | latest             | `mailhog`       | [mailhog/mailhog]                  | ✓       |
| [OpenSMTPD]   | 6.0                | `opensmtpd`     | [anaxexp/opensmtpd]                  |         |
| [Rsyslog]     | latest             | `rsyslog`       | [anaxexp/rsyslog]                    |         |
| Adminer       | 4.6                | `pma`           | [anaxexp/adminer]                    |         |
| phpMyAdmin    | latest             | `pma`           | [phpmyadmin/phpmyadmin]            |         |
| Portainer     | latest             | `portainer`     | [portainer/portainer]              | ✓       |
| Traefik       | latest             | `traefik`       | [_/traefik]                        | ✓       |

Supported WordPress versions: 4

## Documentation

Full documentation is available at https://docs.anaxexp.com/stacks/wordpress/local.

## Beyond local environment

WordPress4Docker is a project designed to help you spin up local environment with docker-compose. If you want to deploy a consistent stack with orchestrations to your own server, check out [![WordPress stack on AnaxExp](https://www.google.com/s2/favicons?domain=anaxexp.com) AnaxExp](https://anaxexp.com/stacks/wordpress).

## Maintenance

We regularly update images used in this stack and release them together, see [releases page](https://github.com/anaxexp/wordpress4docker/releases) for full changelog and update instructions.  

## License

This project is licensed under the MIT open source license.

[Apache]: https://anaxexp.com/stacks/wordpress/docs/containers/apache
[AthenaPDF]: https://anaxexp.com/stacks/wordpress/docs/containers/athenapdf
[Blackfire]: https://anaxexp.com/stacks/wordpress/docs/containers/blackfire
[Mailhog]: https://anaxexp.com/stacks/wordpress/docs/containers/mailhog
[MariaDB]: https://anaxexp.com/stacks/wordpress/docs/containers/mariadb
[Memcached]: https://anaxexp.com/stacks/wordpress/docs/containers/memcached
[Nginx]: https://anaxexp.com/stacks/wordpress/docs/containers/nginx
[Node.js]: https://anaxexp.com/stacks/wordpress/docs/containers/node
[OpenSMTPD]: https://anaxexp.com/stacks/wordpress/docs/containers/opensmtpd
[PHP]: https://anaxexp.com/stacks/wordpress/docs/containers/php
[PostgreSQL]: https://anaxexp.com/stacks/wordpress/docs/containers/postgres
[Redis]: https://anaxexp.com/stacks/wordpress/docs/containers/redis
[Rsyslog]: https://anaxexp.com/stacks/wordpress/docs/containers/rsyslog
[Solr]: https://anaxexp.com/stacks/wordpress/docs/containers/solr
[Varnish]: https://anaxexp.com/stacks/wordpress/docs/containers/varnish
[Webgrind]: https://anaxexp.com/stacks/wordpress/docs/containers/webgrind
[Wordpress]: https://anaxexp.com/stacks/wordpress/docs/containers/php

[_/traefik]: https://hub.docker.com/_/traefik
[arachnysdocker/athenapdf-service]: https://hub.docker.com/r/arachnysdocker/athenapdf-service
[blackfire/blackfire]: https://hub.docker.com/r/blackfire/blackfire
[mailhog/mailhog]: https://hub.docker.com/r/mailhog/mailhog
[phpmyadmin/phpmyadmin]: https://hub.docker.com/r/phpmyadmin/phpmyadmin
[portainer/portainer]: https://hub.docker.com/r/portainer/portainer
[anaxexp/adminer]: https://github.com/anaxexp/adminer
[anaxexp/elasticsearch]: https://github.com/anaxexp/elasticsearch
[anaxexp/kibana]: https://github.com/anaxexp/kibana
[anaxexp/mariadb]: https://github.com/anaxexp/mariadb
[anaxexp/memcached]: https://github.com/anaxexp/memcached
[anaxexp/node]: https://github.com/anaxexp/node
[anaxexp/opensmtpd]: https://github.com/anaxexp/opensmtpd
[anaxexp/php-apache]: https://github.com/anaxexp/php-apache
[anaxexp/postgres]: https://github.com/anaxexp/postgres
[anaxexp/redis]: https://github.com/anaxexp/redis
[anaxexp/rsyslog]: https://github.com/anaxexp/rsyslog
[anaxexp/solr]: https://github.com/anaxexp/solr
[anaxexp/webgrind]: https://hub.docker.com/r/anaxexp/webgrind
[anaxexp/wordpress-nginx]: https://github.com/anaxexp/wordpress-nginx
[anaxexp/wordpress-php]: https://github.com/anaxexp/wordpress-php
[anaxexp/wordpress-varnish]: https://github.com/anaxexp/wordpress-varnish
[anaxexp/wordpress]: https://github.com/anaxexp/wordpress
