docker network create —subnet 11.0.0.0/24 -d overlay network-name:-To create a swarm network
Redis service
docker service create —name redis —hostname redis —network netwok_name redis-to create redid service

Postgres service
docker service create --name db --hostname db -e POSTGRES_USEPR=postgres -e POSTGRES_PASSWORD=postgres --replicas 3 --network nework1 postgres-to create rpostgres service

Vote image
docker service create --name vote --hostname vote --network nework1 -p 1000:80 --replicas 5 ashiqummathoor/votenew

Worker image
docker service create --name worker --hostname worker --network nework1 --replicas 3 ashiqummathoor/workernew

Result image
docker service create --name result --hostname result --network nework1 -p 1001:80 --replicas 3 ashiqummathoor/resultnew
