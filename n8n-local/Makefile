# Start n8n with docker-compose
start:
	docker-compose up -d
.PHONY: start

# Stop n8n
stop:
	docker-compose stop
.PHONY: stop

# Stop and remove containers
down:
	docker-compose down
.PHONY: down

# Restart n8n (useful after config changes)
restart: down start
.PHONY: restart

# View logs
logs:
	docker-compose logs -f n8n
.PHONY: logs

# Update n8n to latest version
update:
	docker-compose pull
	docker-compose down
	docker-compose up -d
.PHONY: update

# Start n8n with tunnel enabled for webhooks
tunnel:
	docker-compose run --rm -p 5678:5678 n8n start --tunnel
.PHONY: tunnel

# Show status
status:
	docker-compose ps
.PHONY: status

# Execute shell in running n8n container
shell:
	docker-compose exec n8n sh
.PHONY: shell

# Clean up volumes (WARNING: This will delete all n8n data)
clean:
	docker-compose down -v
	docker volume rm n8n-local_n8n_data 2>/dev/null || true
.PHONY: clean
