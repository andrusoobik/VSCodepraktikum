# VSCodepraktikum
$ docker run -d -p 8080:8088 -e "SUPERSET_SECRET_KEY=ua9guralfvzioref" --name superset apache/superset


docker exec -it superset superset fab create-admin --username admin --firstname Superset --lastname Admin --email admin@superset.com --password admin

docker exec -it superset superset db upgrade

docker exec -it superset superset load_examples

docker exec -it superset superset init

docker run -d -p 8080:8088 -v ${PWD}:/data:rw -e  "SUPERSET_SECRET_KEY=ua9guralfvzioref" --name superset my/superset.duckdb