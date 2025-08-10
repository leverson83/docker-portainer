# Portainer

Web-based Docker management interface for your homelab.

## Quick Start

1. **Clone this repository:**
   ```bash
   git clone git@github.com:leverson83/docker-portainer.git
   cd docker-portainer
   ```

2. **Edit environment file:**
   ```bash
   cp env.example .env
   nano .env
   # Edit .env with your settings
   ```

3. **Start the service:**
   ```bash
   docker compose up -d
   ```

4. **Access the web interface:**
   - URL: http://your-server:30092
   - First time setup will prompt for admin user creation

## Configuration

- **Port:** 30092
- **Data directory:** `${DATA_PATH}/portainer/data`
- **Docker socket:** `/var/run/docker.sock` (read-only)
- **Database:** SQLite (included)

## Environment Variables

- `TZ` - Timezone (default: Australia/Brisbane)
- `DATA_PATH` - Application data storage path
- `PORT` - Web interface port (default: 30092)

## Features

### Docker Management
- **Container management** - Start, stop, restart containers
- **Image management** - Pull, remove, build images
- **Network management** - Create and manage Docker networks
- **Volume management** - Manage Docker volumes
- **Stack deployment** - Deploy Docker Compose stacks

### Monitoring
- **Resource usage** - CPU, memory, disk usage
- **Container logs** - Real-time log viewing
- **Performance metrics** - Container performance tracking
- **Event history** - Docker daemon events

## Security Notes

- **Docker socket access** - Portainer has read-only access to Docker daemon
- **Admin user** - Create a strong password during first-time setup
- **Network isolation** - Runs on its own bridge network
- **Data persistence** - All configuration stored on your NAS

## Integration

Portainer integrates with all your existing Docker containers:
- **Homarr** - Dashboard management
- **Overseerr** - Media request management
- **Radarr/Sonarr** - Media automation
- **Bazarr** - Subtitle management
- **Prowlarr** - Indexer management
- **Planka** - Project management
- **Dozzle** - Log monitoring

## Notes

- Portainer provides a web-based alternative to command-line Docker management
- All configuration and user data is stored on your NAS for easy backup
- The Docker socket mount allows Portainer to manage all containers on the host
- Perfect for managing your entire homelab Docker infrastructure from a single interface 