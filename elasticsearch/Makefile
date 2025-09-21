.PHONY: elasticsearch kibana elastic-logstash elastic-filebeat

COMPOSE_FILE := compose-elasticsearch.yml

compose-up:
	@echo "Building and running containers in detached mode..."
	docker compose -f $(COMPOSE_FILE) up -d --build
	@echo "All containers started"

compose-down:
	@echo "Shutting down containers..."
	docker compose -f $(COMPOSE_FILE) down
	@echo "All containers stopped"

elasticsearch:
	@echo "Running elasticsearch container..."
	docker compose -f $(COMPOSE_FILE) up elasticsearch

kibana:
	@echo "Running kibana container..."
	docker compose -f $(COMPOSE_FILE) up kibana

elastic-logstash:
	@echo "Running elastic-logstash container..."
	docker compose -f $(COMPOSE_FILE) up elastic-logstash

elastic-filebeat:
	@echo "Running elastic-filebeat container..."
	docker compose -f $(COMPOSE_FILE) up elastic-filebeat
