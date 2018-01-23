# Baan - Boilerplate for Django Projects

## Good to know
- Uses Docker to build an image of your app.
- Uses Postgresql as database by default.
- Configuration moved to environment variables according to 12 Factor Methodology.

## Get started
### Install Docker
1. Install Docker on your machine.
2. Run `docker-compose -f deployment/docker-compose.yml up` from the root folder.

### Setup Database
1. Run `docker ps` to get all the container id's.
2. Open a bash shell on the postgres container by writing `docker exec -ti <CONTAINER_ID> bin/bash`.
3. Run `psql --user postgres` from the bash shell.
4. Run `CREATE DATABASE django OWNER postgres` to create the database that you will use for your app. Replace `django` with your desired database name.
5. Run `\q` and `exit` to exit the shell.

### Setup Environment Variables
1. Create a new file called `/app/.env` and copy the contents from `/app/.env.sample` to the new file.
2. Set the `RDS_DB` value to the name of your newly created database. E.g. "django".
