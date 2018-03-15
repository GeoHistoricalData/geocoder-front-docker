# geocoder-front-docker
The dockerized version of the geocoder-front Web application.

We have a docker compose with 2 docker images: 1 for php, 1 for nginx.

For PHP, we have a separate docker for which you need the following package: php-pgsql php-xml (we had to add a few other things too).

In order to be able to run the front-end, you need to set the following environment variables in the pg_vars.env at the same location as the docker-compose file:
- GEOCODER_PG_HOST (localhost by default)
- GEOCODER_PG_PORT (5432 by default)
- GEOCODER_PG_DBNAME (postgres by default)
- GEOCODER_PG_USER (postgres by default)
- GEOCODER_PG_PASSWORD (postgres by default)

These variables allow the frontend to connect with the postgresql database containing the geohistoricaldata.
For instance, add the following line in the file:
GEOCODER_PG_HOST=176.31.187.44
GEOCODER_PG_PORT=5433
GEOCODER_PG_DBNAME=test
GEOCODER_PG_USER=user
GEOCODER_PG_PASSWORD=password

To run the front end, simply run:
`docker-compose up -d`

