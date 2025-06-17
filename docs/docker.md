### Docker Volumns
Currently we are using docker volumes to store the data for the database. Since it would making deleting of data easier when needed.
Docker creates the volume: Docker will create a named volume called postgres_data and store it in /var/lib/docker/volumes/postgres_data/ on your host system
Volume gets mounted: This volume gets mounted to /var/lib/postgresql/data inside the PostgreSQL container (where Postgres stores its data)

### Secrets in Docker
Avoid using environment variables in docker compose file because then they are exposed via docker inspect and process listing or might appear in logs or error stack.
Instead use secrets to store sensitive data like we did in docker-compose.yml file.
