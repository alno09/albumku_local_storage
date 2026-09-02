# BrangkasHub

Private family media storage infrastructure.

BrangkasHub provides self-hosted storage and remote access for family photos and videos.

## Stack

- Ubuntu Server
- Docker
- Immich
- PostgreSQL
- Redis
- Cloudflare Tunnel

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