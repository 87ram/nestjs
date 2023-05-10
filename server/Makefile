###### TODO: 自分で勉強する

up:
	docker compose build --no-cache
	docker compose up -d
	@make migrate
down:
	docker compose down --remove-orphans
destroy:
	docker compose down --rmi all --volumes --remove-orphans
restart:
	docker compose restart
stop:
	docker compose stop
remake:
	@make destroy
	@make up
generate:
	docker compose exec app npx prisma generate
migrate:
	docker compose exec app npx prisma migrate dev
seed:
	docker compose exec app npx prisma db seed
reset:
	docker compose exec app npx prisma migrate reset