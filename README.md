# geneweb-start

Try out [geneweb master](https://github.com/geneweb/geneweb) as long as [this PR](https://github.com/geneweb/geneweb/pull/13957) hasn't been merged.

The setup has it's origin here:

https://github.com/geneweb/geneweb/pull/1395#issuecomment-1769711477

The docker image is built [here](https://github.com/ftrojahn/geneweb/commits/build-fp)

## Installation


### Requirements

You should have installed docker and docker-compose. See the useful links section further down.

### Get it

```
git clone https://github.com/ftrojahn/geneweb-start.git
cd geneweb-start
```

... or download the `docker-compose.yml` to a new directory, create sub directory `data/` there.

Feel free to fork the repo and adjust to your needs.

## Setup

If applicable, put your GeneWeb export file (.gw) OR your Gedcom file (.ged)
in the folder `data/` as `database.gw` OR `database.ged`. 

If one of those files exist, the database in `data/bases/database.gwb` will be created.
After the import, the file will be renamed to `*.imported`, so no reimport will take place eventually.

If neither file nor `data/bases/database.gwb` exists, an empty database will be created

You can put your settings into `data/bases/database.gwf`, templates, images, language files  in `data/etc/`, `data/lang` etc.

Please, edit the `docker-compose.yml` to

* set the default language 

* set the admin password (i.e. "wizard"/"magicien"), which will otherwise be autocreated: 
    in this case you find it in `data/wizard_passwd` 

* have geneweb restarted automagically or not.

## Start

### to see the log:

`docker-compose up`

### in background as daemon:

`docker-compose up -d`

## Stop

`docker-compose stop` if run in daemon mode. Otherwise hit `Ctrl+C`

## Useful links

* Docker installation
  see the [official guide](https://docs.docker.com/engine/install/)

* Docker compose installation 
    see the [official docker compose standalone guide](https://docs.docker.com/compose/install/standalone/) or
    [official docker compose desktop guide](https://docs.docker.com/compose/install/)

* other Windows De/En:

   https://www.ionos.de/digitalguide/server/konfiguration/docker-windows-11/ 

   https://www.ionos.de/digitalguide/server/konfiguration/docker-compose-auf-windows/

   https://www.ionos.com/digitalguide/server/configuration/install-docker-compose-on-windows/
