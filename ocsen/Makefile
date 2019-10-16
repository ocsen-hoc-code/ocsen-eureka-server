default:
	@echo "=============Building Local Service============="
	./mvnw clean install
	docker build -f Dockerfile -t ocsen-eureka-server .
app:
	@echo "=============Building Local Service============="
	./mvnw clean install

build: default
	@echo "=============Build And Starting Service Locally============="
	docker-compose up -d

up:
	@echo "=============Starting Service Locally============="
	docker-compose up -d

logs:
	docker-compose logs -f

down:
	docker-compose down

test:
	./mvnw test -B

clean: down
	@echo "=============Cleaning Up============="
	rm -f ocsen-eureka-server
	docker system prune -f
	docker volume prune -f
