Copy .env.example to .env and edit info
docker compose up -d
docker-compose exec app composer install
docker-compose exec app php artisan key:generate
docker-compose exec app php artisan config:cache
phpmyadmin : http://127.0.0.1:8080/ 
import db inv.sql
website : http://127.0.0.1/