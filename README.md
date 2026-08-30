# Self-Hosted Servers

## Docker Configurations

This repository contains Docker Compose configurations for setting up a complete self-hosted media server stack:

- **Jellyfin**: Media server for streaming your collection
- **Jellyseerr**: Request management and user interface for your media
- **Radarr**: Movie collection manager
- **Sonarr**: TV show collection manager
- **Prowlarr**: Indexer manager for torrent/NZB searches
- **Bazarr**: Subtitle management
- **Heimdall**: Application dashboard
- **FileBrowser**: Web-based file manager
- **Dozzle**: Real-time Docker log viewer
- **Watchtower**: Automatic Docker container updates
- **Gluetun**: VPN client for secure networking. In this config also has configs for tramsmission, which will be the main torrent app.

All configurations use the `{{ CHANGE ME }}` placeholder for volume mappings that need to be customized for your environment.

## Prerequisites

### Installing Docker CE (Ubuntu)

To use these configurations, you'll need Docker and Docker Compose installed:

**Ubuntu/Debian:**

`https://docs.docker.com/engine/install/ubuntu/`

```bash
# Add your user to the docker group (log out and back in after this)
sudo usermod -aG docker $USER
```

### Installing Portainer

Portainer provides a web-based UI for managing your Docker containers:

`https://docs.portainer.io/start/install-ce/server/docker/linux`

Portainer will be accessible at `https://your-server-ip:9443`

## Usage

1. Clone this repository
2. Edit the Docker Compose files to replace `{{ CHANGE ME }}` with your actual paths
3. Run the services you want by goign to portainer -> Node -> Stack -> Add stack

## Configuration Notes

- All services are configured with appropriate restart policies
- Timezone is set to America/New_York in most configurations (change as needed)
- Volume mappings need to be customized for your specific setup
- Most services expose their default ports (modify if needed)
