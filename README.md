# Automated Homelab Media Infrastructure

Production-ready, containerized self-hosted media server and automation stack deployed on Ubuntu Server LTS using Docker Compose.

---

## Architecture Overview

* **Jellyfin**: Hardware-accelerated media streaming server.
* **Sonarr**: Automated TV series monitoring and management.
* **Prowlarr**: Centralized indexer and tracker proxy manager.
* **qBittorrent**: Headless BitTorrent client for media acquisition.
* **Jellyseerr**: Request and discovery frontend for streaming services.

---

## Storage Layout

Standardized paths mounted across containers for zero-overhead moves:

* `/data/shows` - TV series library
* `/data/anime` - Anime library
* `/data/torrents` - Incomplete and complete downloads

---

## Deployment

```bash
# Deploy services
docker compose up -d

# Check service status
docker compose ps
```

---

## Security & Configuration

* Sensitive runtime data and tokens isolated via `.gitignore`.
* Configured with dedicated `PUID` and `PGID` permissions.
