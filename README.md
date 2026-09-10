# Albumku

Self-hosted family photo and video storage.

Albumku provides private, self-hosted storage and remote access for family photos and videos.

## Stack

* Ubuntu Server
* Docker
* Immich
* PostgreSQL
* Valkey
* Cloudflare Tunnel

## Repository Scope

This repository contains deployment configuration only.

Application data, media files, databases, credentials, and other runtime data are not stored in Git.

## Planned Architecture

```text
Internet
   |
Cloudflare
   |
Cloudflare Tunnel
   |
ThinkCentre
   |
Immich
   |
Media Storage
```

## Storage

Persistent storage is separated from the application configuration:

```text
SSD
└── PostgreSQL

External HDD
└── Immich Library
```

The Immich library is mounted from:

```text
/srv/albumku/library
```

Database storage remains on the ThinkCentre's internal SSD.
