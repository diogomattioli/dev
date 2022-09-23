# docker-compose.yml

General `docker-compose.yml` file for local development containing several configured services and their respective admin ui.

The admin ui uses the same port number as the service, however the last 2 digits are replaced with 80 (postgres 5432 -> postgres-admin 5480).

Usage: `docker-compose -f FILE -p PROFILE create [SERVICES]`

## Example

Configuring a local environment for a profile called  `my_project` with services postgres, redis, grafana and their admin ui.

Creating: `docker-compose -f /path/to/docker-compose.yml -p my_project create postgres postgres-admin redis redis-admin grafana`

Starting: `docker-compose -p my_project start`

Stopping: `docker-compose -p my_project stop`

Removing: `docker-compose -p my_project down`
