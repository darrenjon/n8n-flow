# n8n Self-Hosted Setup with PostgreSQL

This repository contains the configuration for self-hosting [n8n](https://n8n.io/), a workflow automation tool, using Docker Compose and PostgreSQL as the database. The setup uses the Taipei timezone (`Asia/Taipei`).

## Prerequisites
- **Docker Desktop**: Installed and running on macOS/Windows.
- **Docker Compose**: Installed with Docker Desktop.
- **Git**: Installed for version control.
- **Future Extensions** (optional):
  - Redis: For AI memory caching.
  - Qdrant: For vector database support.

## Setup Instructions
### 1. Clone the Repository

### 2. Create a `.env` File from example env file

```bash
cp .env.example .env
```

### 3. Update the `.env` File
Update the `.env` file with your desired values.
- Replace with your own username, password, and database name etc.

### 4. Start the Docker Services

```bash
docker-compose up -d
```
- Wait for n8n and postgres images to download and start.
- Check status: `docker compose ps`

### 5. Access n8n

- Open `http://localhost:5678/` in your browser.
- Register a new account (e.g., yourname@example.com and a secure password).
- Log in to start using n8n.

## Useful Commands

- **Start Services**: `docker compose up -d`
- **Stop Services**: `docker compose down`
- **View Logs**: `docker compose logs -f`
- **Restart Services**: `docker compose restart`
- **Update Services**: `docker compose pull && docker compose up -d`
- **Full reset (remove data)**: `docker compose down -v`

## License
Base on n8n's Sustainable Use License [license](https://github.com/n8n-io/n8n/tree/master?tab=License-1-ov-file)