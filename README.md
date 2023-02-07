# Kafka Connector Demo

## Services

[List of Services](./docs/SERVICES.md)

## Tooling

[List of tools to run this repo](./docs/TOOLING.md)

## Running a Task

Run the command `task` from the project root to get a list of all available tasks to run.
For example: `task dc:local-up`.

## Running against a staging DB

If you want to run against another database, copy `.example.env` and rename it to `.stage.env`.
Fill out the env file with the necessary values.
Make sure you can reach the database at `localhost:3306` with a tunnel or proxy or other means.
Run `task dc:stage-up`.

### Example: Open SSH Tunnel to DB

One way to connect to the target database is to open an SSH tunnel.
For example:

```bash
ssh -o StrictHostKeyChecking=no -L 3306:${STAGE_DB_HOST}:3306 ${SSH_USER}@${SSH_HOST}
```

This will open a tunnel as `SSH_USER@SSH_HOST` through `STAGE_DB_HOST:3306`.
The database will be available at `localhost:3306`.

## References

- [ConfluentInc All-In-One Community Edition Demo Repo](https://github.com/confluentinc/cp-all-in-one/tree/7.3.0-post/cp-all-in-one-community)
- [Confluent Demo: Connector Zero to Hero Repo](https://github.com/confluentinc/demo-scene/tree/master/kafka-connect-zero-to-hero)
- [Docker Image Reference](https://docs.confluent.io/platform/current/installation/docker/image-reference.html#docker-image-reference-for-cp)
