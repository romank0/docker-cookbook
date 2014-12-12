
## Postgres

Run
```
docker run --name some-postgres -e POSTGRES_PASSWORD=password -d postgres
```

Connect with psql

```
docker run -it --link some-postgres:postgres --rm postgres sh -c 'exec psql -h "$POSTGRES_PORT_5432_TCP_ADDR" -p "$POSTGRES_PORT_5432_TCP_PORT" -U postgres'
```

More [documentation](https://registry.hub.docker.com/_/postgres/).
