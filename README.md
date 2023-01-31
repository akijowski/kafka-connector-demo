# Kafka Connector Demo

## Services

[List of Services](./docs/SERVICES.md)

## Tooling

[List of tools to run this repo](./docs/TOOLING.md)

## Running against a staging DB

If you want to run against another database, copy `.example.env` and rename it to `.stage.env`.
Fill out the env file with the necessary values.
Make sure you can reach the database at `localhost:3306` with a tunnel or proxy or other means.
Run `task dc-stage-up`.

## References

- [ConfluentInc All-In-One Community Edition Demo Repo](https://github.com/confluentinc/cp-all-in-one/tree/7.3.0-post/cp-all-in-one-community)
- [Confluent Demo: Connector Zero to Hero Repo](https://github.com/confluentinc/demo-scene/tree/master/kafka-connect-zero-to-hero)
- [Docker Image Reference](https://docs.confluent.io/platform/current/installation/docker/image-reference.html#docker-image-reference-for-cp)
