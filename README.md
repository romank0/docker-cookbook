
## Java

```
docker run -it --rm dockerfile/java:oracle-java8 java -version
```

Versions:
- latest (default): openjdk-7-jre
- openjdk-6-jdk
- openjdk-6-jre
- openjdk-7-jdk
- openjdk-7-jre
- oracle-java6
- oracle-java7
- oracle-java8 

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
