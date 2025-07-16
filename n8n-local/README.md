# n8n Local Setup

A simple Docker Compose setup for running n8n locally with SQLite database.

## Quick Start

```bash
make start
```

Access n8n at: http://localhost:5678

## Available Commands

- `make start` - Start n8n in detached mode
- `make stop` - Stop n8n container
- `make down` - Stop and remove containers
- `make logs` - View n8n logs
- `make status` - Show container status
- `make update` - Update n8n to latest version
- `make tunnel` - Start n8n with tunnel for webhooks
- `make clean` - Remove all data (⚠️ WARNING: Deletes all workflows and data)

## Webhooks

For external webhooks to work, use the tunnel command:

```bash
make tunnel
```

This enables n8n's tunnel service for webhook access from external services.

## Data Persistence

Workflow data is stored in a Docker volume (`n8n_data`) and persists between container restarts.
