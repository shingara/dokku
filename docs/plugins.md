# Plugins

Dokku itself is built out of plugins and uses [plugn](https://github.com/dokku/plugn) for its plugin system. In essence a plugin is a collection of scripts that will be run based on naming convention.

Let's take a quick look at the current dokku nginx plugin that's shipped with dokku by default.

    nginx-vhosts/
    ├── plugin.toml  # plugin metadata
    ├── commands     # contains additional commands
    ├── install      # runs on dokku installation
    └── post-deploy  # runs after an app is deployed

## Installing a plugin

```shell
# This command requires `root` permissions as the `install` and `install-dependencies`
# plugin triggers may utilize commands such as `apt-get`. For non-core plugins, please
# inspect those plugins before running the following command as `root` user.
sudo dokku plugin:install <git_url>

# previous versions (0.3.x and below) of dokku require a manual process to install plugins
cd /var/lib/dokku/plugins
git clone <git url>
dokku plugins-install
```

## Creating your own plugin

[See the full documentation](http://dokku.viewdocs.io/dokku/development/plugin-creation).

## Official Plugins (Beta)

The following plugins are available and provided by dokku maintainers. Where noted, these plugins should be considered beta software and may not have been used as thoroughly as community plugins. Please file issues against their respective issue trackers.

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [CouchDB (beta)](https://github.com/dokku/dokku-couchdb)                                          | [dokku][]             | 0.4.0+                |
| [Elasticsearch (beta)](https://github.com/dokku/dokku-elasticsearch-plugin)                       | [dokku][]             | 0.4.0+                |
| [MariaDB (beta)](https://github.com/dokku/dokku-mariadb-plugin)                                   | [dokku][]             | 0.4.0+                |
| [Memcached (beta)](https://github.com/dokku/dokku-memcached-plugin)                               | [dokku][]             | 0.4.0+                |
| [Mongo (beta)](https://github.com/dokku/dokku-mongo-plugin)                                       | [dokku][]             | 0.4.0+                |
| [MySQL (beta)](https://github.com/dokku/dokku-mysql-plugin)                                       | [dokku][]             | 0.4.0+                |
| [Nats (beta)](https://github.com/dokku/dokku-nats)                                                | [dokku][]             | 0.4.0+                |
| [Postgres (beta)](https://github.com/dokku/dokku-postgres-plugin)                                 | [dokku][]             | 0.4.0+                |
| [RabbitMQ (beta)](https://github.com/dokku/dokku-rabbitmq-plugin)                                 | [dokku][]             | 0.4.0+                |
| [Redis (beta)](https://github.com/dokku/dokku-redis-plugin)                                       | [dokku][]             | 0.4.0+                |
| [RethinkDB (beta)](https://github.com/dokku/dokku-rethinkdb-plugin)                               | [dokku][]             | 0.4.0+                |
| [Copy Files to Image](https://github.com/dokku/dokku-copyfiles-to-image)                          | [dokku][]             | 0.4.0+                |
| [HTTP Auth (beta)](https://github.com/dokku/dokku-http-auth)                                      | [dokku][]             | 0.4.0+                |
| [Maintenance mode (beta)](https://github.com/dokku/dokku-maintenance)                             | [dokku][]             | 0.4.0+                |
| [Redirect (beta)](https://github.com/dokku/dokku-redirect)                                        | [dokku][]             | 0.4.0+                |

## Community plugins

Note: The following plugins have been supplied by our community and may not have been tested by dokku maintainers.

[256dpi]: https://github.com/256dpi
[abossard]: https://github.com/dudagroup
[ademuk]: https://github.com/ademuk
[agco-adm]: https://github.com/agco-adm
[alessio]: https://github.com/alessio
[alex-sherwin]: https://github.com/alex-sherwin
[alexanderbeletsky]: https://github.com/alexanderbeletsky
[alexkruegger]: https://github.com/alexkruegger
[Aomitayo]: https://github.com/Aomitayo
[apmorton]: https://github.com/apmorton
[Benjamin-Dobell]: https://github.com/Benjamin-Dobell
[blag]: https://github.com/blag
[cameron-martin]: https://github.com/cameron-martin
[cedricziel]: https://github.com/cedricziel
[cef]: https://github.com/cef
[cjblomqvist]: https://github.com/cjblomqvist
[darkpixel]: https://github.com/darkpixel
[dokku]: https://github.com/dokku
[dyson]: https://github.com/dyson
[F4-Group]: https://github.com/F4-Group
[fermuch]: https://github.com/fermuch
[fgrehm]: https://github.com/fgrehm
[Flink]: https://github.com/Flink
[gdi2290]: https://github.com/gdi2290
[heichblatt]: https://github.com/heichblatt
[hughfletcher]: https://github.com/hughfletcher
[ignlg]: https://github.com/ignlg
[iskandar]: https://github.com/iskandar
[jagandecapri]: https://github.com/jagandecapri
[jeffutter]: https://github.com/jeffutter
[jlachowski]: https://github.com/jlachowski
[Kloadut]: https://github.com/Kloadut
[krisrang]: https://github.com/krisrang
[luxifer]: https://github.com/luxifer
[Maciej Łebkowski]: https://github.com/mlebkowski
[matto1990]: https://github.com/matto1990
[mbriskar]: https://github.com/mbriskar
[michaelshobbs]: https://github.com/michaelshobbs
[mikecsh]: https://github.com/mikecsh
[mikexstudios]: https://github.com/mikexstudios
[mixxorz]: https://github.com/mixxorz
[mlebkowski]: https://github.com/mlebkowski
[motin]: https://github.com/motin
[musicglue]: https://github.com/musicglue
[neam]: https://github.com/neam
[nickstenning]: https://github.com/nickstenning
[nornagon]: https://github.com/nornagon
[ohardy]: https://github.com/ohardy
[pauldub]: https://github.com/pauldub
[pnegahdar]: https://github.com/pnegahdar
[RaceHub]: https://github.com/racehub
[ribot]: https://github.com/ribot
[rlaneve]: https://github.com/rlaneve
[robv]: https://github.com/robv
[scottatron]: https://github.com/scottatron
[sehrope]: https://github.com/sehrope
[sekjun9878]: https://github.com/sekjun9878
[sgulseth]: https://github.com/sgulseth
[sseemayer]: https://github.com/sseemayer
[statianzo]: https://github.com/statianzo
[stuartpb]: https://github.com/stuartpb
[thrashr888]: https://github.com/thrashr888
[wmluke]: https://github.com/wmluke
[Zenedith]: https://github.com/Zenedith

### Datastores

#### Relational

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [MariaDB](https://github.com/Kloadut/dokku-md-plugin)                                             | [Kloadut][]           | 0.3.x                  |
| [MariaDB (single container)](https://github.com/ohardy/dokku-mariadb)                             | [ohardy][]            | 0.3.x                  |
| [MariaDB (single container)](https://github.com/krisrang/dokku-mariadb)                           | [krisrang][]          | 0.3.26+                |
| [PostgreSQL](https://github.com/jlachowski/dokku-pg-plugin)                                       | [jlachowski][]         | 0.3.x                  |
| [PostgreSQL (single container)](https://github.com/ohardy/dokku-psql)                             | [ohardy][]            | 0.3.x                  |
| [PostgreSQL (single container)](https://github.com/Flink/dokku-psql-single-container)             | [Flink][]             | 0.3.26+                |

#### Caching

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [Redis](https://github.com/sekjun9878/dokku-redis-plugin)                                         | [sekjun9878][]         | 0.3.26+                |
| [Redis (single container)](https://github.com/ohardy/dokku-redis)                                 | [ohardy][]            | 0.3.x                  |
| [Varnish](https://github.com/Zenedith/dokku-varnish-plugin)                                       | [Zenedith][]          | Varnish cache between nginx and application with base configuration|

#### Queuing

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [RabbitMQ](https://github.com/jlachowski/dokku-rabbitmq-plugin)                                   | [jlachowski][]        | 0.3.x                 |
| [RabbitMQ (single container)](https://github.com/jlachowski/dokku-rabbitmq-single-plugin)         | [jlachowski][]        | 0.3.x                 |

#### Other

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [RethinkDB](https://github.com/stuartpb/dokku-rethinkdb-plugin)                                   | [stuartpb][]          | 0.3.x                  |

[dccee02]: https://github.com/jeffutter/dokku-riakcs-plugin/commit/dccee02702e7001851917b7814e78a99148fb709

### Process Managers

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [Circus](https://github.com/apmorton/dokku-circus)                                                | [apmorton][]          |                       |
| [Forego](https://github.com/iskandar/dokku-forego)                                                | [iskandar][]          | Compatible with 0.2.x |
| [Forego](https://github.com/Flink/dokku-forego)                                                   | [Flink][]             | 0.4.0+                |
| [Logging Supervisord](https://github.com/sehrope/dokku-logging-supervisord)                       | [sehrope][]           | 0.4.0+                |
| [Monit](https://github.com/cjblomqvist/dokku-monit)                                               | [cjblomqvist][]       | 0.3.x                 |
| [Shoreman ](https://github.com/statianzo/dokku-shoreman)                                          | [statianzo][]         | 0.3.x                 |
| [Supervisord](https://github.com/statianzo/dokku-supervisord)                                     | [statianzo][]         | 0.3.x                 |

[c77cbf1]: https://github.com/dokku/dokku/commit/c77cbf1d3ae07f0eafb85082ed7edcae9e836147
[28de3ec]: https://github.com/dokku/dokku/commit/28de3ecaa3231a223f83fd8d03f373308673bc40

### Dokku Features

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [App name as env](https://github.com/cjblomqvist/dokku-app-name-env)                              | [cjblomqvist][]       | 0.3.x                 |
| [Docker Direct](https://github.com/heichblatt/dokku-docker-direct)                                | [heichblatt][]        |                       |
| [Dokku Copy App Config Files](https://github.com/alexkruegger/dokku-app-configfiles)              | [alexkruegger][]      | Compatible with 0.3.17+ |
| [Dokku Copy App Config Files](https://github.com/heichblatt/dokku-supply-config)                  | [heichblatt][]        |                       |
| [Dokku Name](https://github.com/alex-sherwin/dokku-name)                                          | [alex-sherwin][]      | dokku >= [c77cbf1][]  |
| [Dokku Registry](https://github.com/agco-adm/dokku-registry)<sup>1</sup>                          | [agco-adm][]          | 0.4.0+                |
| [git rev-parse HEAD in env](https://github.com/cjblomqvist/dokku-git-rev)                         | [cjblomqvist][]       | 0.4.0+                |
| [Graduate (Environment Management)](https://github.com/glassechidna/dokku-graduate)               | [Benjamin-Dobell][]   | 0.3.14+               |
| [Haproxy tcp load balancer](https://github.com/256dpi/dokku-haproxy)                              | [256dpi][]            | 0.4.0+                |
| [HTTP Auth Secure Apps](https://github.com/matto1990/dokku-secure-apps)                           | [matto1990][]         | 0.4.0+                |
| [Hostname](https://github.com/michaelshobbs/dokku-hostname)                                       | [michaelshobbs][]     | 0.4.0+                |
| [Lets Encrypt](https://github.com/sseemayer/dokku-letsencrypt)                                    | [sseemayer][]         | 0.4.0+                |
| [Multi-Buildpack](https://github.com/pauldub/dokku-multi-buildpack)                               | [pauldub][]           |                       |
| [Nuke Containers](https://github.com/heichblatt/dokku-nuke)                                       | [heichblatt][]        |                       |
| [Open App Ports](https://github.com/heichblatt/dokku-ports)                                       | [heichblatt][]        |                       |
| [Pre-Deploy Tasks](https://github.com/michaelshobbs/dokku-app-predeploy-tasks)                    | [michaelshobbs][]     | 0.4.0+                |
| [SSH Deployment Keys](https://github.com/cedricziel/dokku-deployment-keys)<sup>2</sup>            | [cedricziel][]        | 0.3.x                 |
| [SSH Hostkeys](https://github.com/cedricziel/dokku-hostkeys-plugin)<sup>3</sup>                   | [cedricziel][]        | 0.3.x                 |
| [Volume (persistent storage)](https://github.com/ohardy/dokku-volume)                             | [ohardy][]            | 0.3.x                 |

[217d00a]: https://github.com/dokku/dokku/commit/217d00a1bc47a7e24d8847617bb08a1633025fc7

<sup>1</sup> On Heroku similar functionality is offered by the [heroku-labs pipeline feature](https://devcenter.heroku.com/articles/labs-pipelines), which allows you to promote builds across multiple environments (staging -> production)

<sup>2</sup> Adds the possibility to add SSH deployment keys to receive private hosted packages

<sup>3</sup> Adds the ability to add custom hosts to the containers known_hosts file to be able to ssh them easily (useful with deployment keys)

### Other Plugins

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [Airbrake deploy](https://github.com/Flink/dokku-airbrake-deploy)                                 | [Flink][]             | 0.4.0+                |
| [APT](https://github.com/F4-Group/dokku-apt)                                                      | [F4-Group][]          | 0.2.0+ (tag 0.2.0), 0.3.0+ (tag 0.3.0), 0.4.0+ |
| [Chef cookbooks](https://github.com/fgrehm/chef-dokku)                                            | [fgrehm][]            |                       |
| [Bower install](https://github.com/alexanderbeletsky/dokku-bower-install)                         | [alexanderbeletsky][] |                       |
| [Bower/Grunt](https://github.com/thrashr888/dokku-bower-grunt-build-plugin)                       | [thrashr888][]        |                       |
| [Bower/Gulp](https://github.com/gdi2290/dokku-bower-gulp-build-plugin)                            | [gdi2290][]           |                       |
| [Bower/Gulp](https://github.com/jagandecapri/dokku-bower-gulp-build-plugin)                       | [jagandecapri][]      |                       |
| [Builders: bower, compass, gulp, grunt](https://github.com/ignlg/dokku-builders-plugin)           | [ignlg][]             | 0.4.0+                |
| [Docker auto persist volumes](https://github.com/Flink/dokku-docker-auto-volumes)                 | [Flink][]             | 0.4.0+                |
| [HipChat Notifications](https://github.com/cef/dokku-hipchat)                                     | [cef][]               |                       |
| [Graphite/statsd](https://github.com/jlachowski/dokku-graphite-plugin)                            | [jlachowski]          | <0.4.0                |
| [Graphite/statsd](https://github.com/jlachowski/dokku-graphite-grafana)                           | [jlachowski]          | 0.4.0+, graphite & statsd plugin with grafana dashboard frontend  |
| [Logspout](https://github.com/michaelshobbs/dokku-logspout)                                       | [michaelshobbs][]     | 0.3.26+               |
| [Node](https://github.com/pnegahdar/dokku-node)                                                   | [pnegahdar][]         |                       |
| [Node](https://github.com/ademuk/dokku-nodejs)                                                    | [ademuk][]            |                       |
| [Reset mtime](https://github.com/mixxorz/dokku-docker-reset-mtime)                                | [mixxorz][]           | 0.3.15+, Dockerfile support |
| [Slack Notifications](https://github.com/ribot/dokku-slack)                                       | [ribot][]             | 0.4.0+                |
| [User ACL](https://github.com/mlebkowski/dokku-acl)                                               | [Maciej Łebkowski][]  | 0.4.0+                |
| [Webhooks](https://github.com/nickstenning/dokku-webhooks)                                        | [nickstenning][]      |                       |
| [Wkhtmltopdf](https://github.com/mbriskar/dokku-wkhtmltopdf)                                      | [mbriskar][]          |                       |
| [Wordpress](https://github.com/dudagroup/dokku-wordpress-template)                                | [abossard][]          | Dokku dev, mariadb, volume, domains |

<sup>1</sup> Forked from [jezdez/dokku-elasticsearch-plugin](https://github.com/jezdez/dokku-elasticsearch-plugin): uses Elasticsearch 1.2 (instead of 0.90), doesn't depend on dokku-link, runs as elasticsearch user instead of root, and turns off multicast autodiscovery for use in a VPS environment.

### Deprecated Plugins

The following plugins have been removed as their functionality is now in Dokku Core.

| Plugin                                                                                            | Author                | In Dokku Since                  |
| ------------------------------------------------------------------------------------------------- | --------------------- | ------------------------------- |
| [Custom Domains](https://github.com/neam/dokku-custom-domains)                                    | [motin][]             | v0.3.10 (domains plugin)        |
| [Debug](https://github.com/heichblatt/dokku-debug)                                                | [heichblatt][]        | v0.3.9 (trace command)          |
| [Docker Options](https://github.com/dyson/dokku-docker-options)                                   | [dyson][]             | v0.3.17 (docker-options plugin) |
| [Events Logger](https://github.com/alessio/dokku-events)                                          | [alessio][]           | v0.3.21 (events plugin)         |
| [Host Port binding](https://github.com/stuartpb/dokku-bind-port)                                  | [stuartpb][]          | v0.3.17 (docker-options plugin) |
| [List Containers](https://github.com/heichblatt/dokku-list)                                       | [heichblatt][]        | v0.3.14 (ps plugin              |
| [Link Containers](https://github.com/rlaneve/dokku-link)                                          | [rlaneve][]           | v0.3.17 (docker-options plugin) |
| [Multiple Domains](https://github.com/wmluke/dokku-domains-plugin)<sup>1</sup>                    | [wmluke][]            | v0.3.10 (domains plugin)        |
| [Named-containers](https://github.com/Flink/dokku-named-containers)                               | [Flink][]             | v0.4.2 (named-containers plugin) |
| [Nginx-Alt](https://github.com/mikexstudios/dokku-nginx-alt)                                      | [mikexstudios][]      | v0.3.10 (domains plugin)        |
| [Persistent Storage](https://github.com/dyson/dokku-persistent-storage)                           | [dyson][]             | v0.3.17 (docker-options plugin) |
| [PrimeCache](https://github.com/darkpixel/dokku-prime-cache)                                      | [darkpixel][]         | v0.3.0 (zero downtime deploys)  |
| [Rebuild application](https://github.com/scottatron/dokku-rebuild)                                | [scottatron][]        | v0.3.14 (ps plugin)             |
| [Supply env vars to buildpacks](https://github.com/cameron-martin/dokku-build-env)<sup>2</sup>    | [cameron-martin][]    | v0.3.9 (build-env plugin)       |
| [user-env-compile](https://github.com/musicglue/dokku-user-env-compile)<sup>2</sup>               | [musicglue][]         | v0.3.9 (build-env plugin)       |
| [user-env-compile](https://github.com/motin/dokku-user-env-compile)<sup>2</sup>                   | [motin][]             | v0.3.9 (build-env plugin)       |
| [VHOSTS Custom Configuration](https://github.com/neam/dokku-nginx-vhosts-custom-configuration)    | [motin][]             | v0.3.10 (domains plugin)        |

<sup>1</sup> Conflicts with [VHOSTS Custom Configuration](https://github.com/neam/dokku-nginx-vhosts-custom-configuration)
<sup>2</sup> Similar to the heroku-labs feature (see https://devcenter.heroku.com/articles/labs-user-env-compile)

[a043e98]: https://github.com/stuartpb/dokku-bind-port/commit/a043e9892f4815b6525c850131e09fd64db5c1fa


### Unmaintained Plugins

The following plugins are no longer maintained by their developers.

| Plugin                                                                                            | Author                | Compatibility         |
| ------------------------------------------------------------------------------------------------- | --------------------- | --------------------- |
| [app-url](https://github.com/mikecsh/dokku-app-url)                                               | [mikecsh][]           | Works with 0.2.0      |
| [CouchDB (multi containers)](https://github.com/Flink/dokku-couchdb-multi-containers)             | [Flink][]             | 0.4.0+                |
| [CouchDB](https://github.com/racehub/dokku-couchdb-plugin)                                        | [RaceHub][]           | Compatible with 0.2.0 |
| [Elasticsearch](https://github.com/robv/dokku-elasticsearch)                                      | [robv][]              | Not compatible with >= 0.3.0 (still uses /home/git) |
| [Elasticsearch](https://github.com/blag/dokku-elasticsearch-plugin)<sup>1</sup>                   | [blag][]              | Compatible with 0.2.0 |
| [Memcached](https://github.com/Flink/dokku-memcached-plugin)                                      | [Flink][]             | 0.4.0+                |
| [MongoDB (single container)](https://github.com/jeffutter/dokku-mongodb-plugin)                   | [jeffutter][]         |                       |
| [MySQL](https://github.com/hughfletcher/dokku-mysql-plugin)                                       | [hughfletcher][]      |                       |
| [Neo4j](https://github.com/Aomitayo/dokku-neo4j-plugin)                                           | [Aomitayo][]          |                       |
| [PostGIS](https://github.com/fermuch/dokku-pg-plugin)                                             | [fermuch][]           |                       |
| [PostgreSQL (single container)](https://github.com/jeffutter/dokku-postgresql-plugin)             | [jeffutter][]         | This plugin creates a single postgresql container that all your apps can use. Thus only one instance of postgresql running (good for servers without a ton of memory). |
| [RiakCS (single container)](https://github.com/jeffutter/dokku-riakcs-plugin)                     | [jeffutter][]         | Incompatible with 0.2.0 (checked at [dccee02][]) |
| [Redis](https://github.com/luxifer/dokku-redis-plugin)                                            | [luxifer][]           |                       |
