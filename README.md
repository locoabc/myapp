# Welcome to Loco :train: test


Loco is a web and API framework running on Rust.

This is the **SaaS starter** which includes a `User` model and authentication based on JWT.

This source repo is for (Getting Started)(https://github.com/loco-rs/loco/blob/master/docs-site/content/docs/getting-started/guide.md)

## Quick Start

Docker environment setup

```
[me@rocky9t01a myapp]$ tree -aL 1  .devcontainer/
.devcontainer/
├── devcontainer.json
├── docker-compose.yml
├── Dockerfile
└── .env

0 directories, 4 files
[me@rocky9t01a myapp]$ cat .devcontainer/.env
POSTGRES_DB=loco_app
POSTGRES_USER=loco
POSTGRES_PASSWORD=loco
DATABASE_URL=postgres://loco:loco@db:5432/loco_app
REDIS_URL=redis://redis:6379
MAILER_HOST=mailer[me@rocky9t01a myapp]$


```

start and stop :


```
docker-compose up -d 
docker-compose --volume # --volume is to remove db data volume.
```
You need:

* A local postgres instance
* A local Redis instance

Check out your development [configuration](config/development.yaml).

> To configure a database , please run a local postgres database with <code>loco:loco</code> and a db named <code>[app name]_development.</code>: 
<code>docker run -d -p 5432:5432 -e POSTGRES_USER=loco -e POSTGRES_DB=[app name]_development -e POSTGRES_PASSWORD="loco" postgres:15.3-alpine</code>

Now start your app:

```
$ cargo loco start
Finished dev [unoptimized + debuginfo] target(s) in 21.63s
    Running `target/debug/myapp start`

    :
    :
    :

controller/app_routes.rs:203: [Middleware] Adding log trace id

                      ▄     ▀
                                 ▀  ▄
                  ▄       ▀     ▄  ▄ ▄▀
                                    ▄ ▀▄▄
                        ▄     ▀    ▀  ▀▄▀█▄
                                          ▀█▄
▄▄▄▄▄▄▄  ▄▄▄▄▄▄▄▄▄   ▄▄▄▄▄▄▄▄▄▄▄ ▄▄▄▄▄▄▄▄▄ ▀▀█
 ██████  █████   ███ █████   ███ █████   ███ ▀█
 ██████  █████   ███ █████   ▀▀▀ █████   ███ ▄█▄
 ██████  █████   ███ █████       █████   ███ ████▄
 ██████  █████   ███ █████   ▄▄▄ █████   ███ █████
 ██████  █████   ███  ████   ███ █████   ███ ████▀
   ▀▀▀██▄ ▀▀▀▀▀▀▀▀▀▀  ▀▀▀▀▀▀▀▀▀▀  ▀▀▀▀▀▀▀▀▀▀ ██▀
       ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀

started on port 3000
```

## Getting help

Check out [a quick tour](https://loco.rs/docs/getting-started/tour/) or [the complete guide](https://loco.rs/docs/getting-started/guide/).
# myapp
