.PHONY: opensearch opensearch-dashboards opensearch-logstash opensearch-filebeat

COMPOSE_FILE := compose-opensearch.yml

compose-up:
	@echo "Building and running containers in detached mode..."
	docker compose -f $(COMPOSE_FILE) up -d --build
	@echo "All containers started"

compose-down:
	@echo "Shutting down containers..."
	docker compose -f $(COMPOSE_FILE) down
	@echo "All containers stopped"

opensearch:
	@echo "Running opensearch container..."
	docker compose -f $(COMPOSE_FILE) up opensearch

opensearch-dashboards:
	@echo "Running opensopensearch-dashboards container..."
	docker compose -f $(COMPOSE_FILE) up opensearch-dashboards

opensearch-logstash:
	@echo "Running opensearch-logstash container..."
	docker compose -f $(COMPOSE_FILE) up opensearch-logstash

opensearch-filebeat:
	@echo "Running opensearch-filebeat container..."
	docker compose -f $(COMPOSE_FILE) up opensearch-filebeat
