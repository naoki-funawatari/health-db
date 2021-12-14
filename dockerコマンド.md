docker-compose down
docker-compose build --no-cache
docker-compose up -d

docker network create health-networks

docker exec -it health-db /bin/sh
docker exec -it health-db /bin/bash

psql -U postgres -d postgres
psql -U health -d healthes
