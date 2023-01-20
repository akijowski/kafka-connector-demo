# Kafka Connector Demo

### References

- [ConfluentInc All-In-One Community Edition Demo Repo](https://github.com/confluentinc/cp-all-in-one/tree/7.3.0-post/cp-all-in-one-community)
- [Confluent Demo: Connector Zero to Hero Repo](https://github.com/confluentinc/demo-scene/tree/master/kafka-connect-zero-to-hero)
- [Docker Image Reference](https://docs.confluent.io/platform/current/installation/docker/image-reference.html#docker-image-reference-for-cp)

## Zookeeper

The necessary evil that allows Kafka to run as a distributed multi-leader service.

### Image
https://hub.docker.com/r/confluentinc/cp-zookeeper

## Kafka Broker

The "vanilla" Kafka broker.
This example only runs a single instance of Kafka, so no replication.
Obviously don't run this in production.

### Image
https://hub.docker.com/r/confluentinc/cp-kafka

## Kafka Schema Registry

Provides centralized management of message schemas for Kafka consumers and producers.
Many Kafka plugins require or heavily recommend using this service.

### Image
https://hub.docker.com/r/confluentinc/cp-schema-registry

## Kafka REST Proxy

A RESTful convenience to inspect and manage Kafka.

### Image
https://hub.docker.com/r/confluentinc/cp-kafka-rest

### API Reference
https://docs.confluent.io/platform/current/kafka-rest/api.html#crest-long-api-reference

## Confluent Control Center

A convenient UI to inspect the Kafka cluster.

### Image
https://hub.docker.com/r/confluentinc/cp-enterprise-control-center

### URL
http://localhost:9021/clusters

## Kafka Connect Debezium

The Kafka Connect cluster (single instance).
The cluster can run more than a single connector, but right now is only configured to run the Debezium config.
The Debezium connector is installed at runtime but there are other methods.

### Image
https://hub.docker.com/r/confluentinc/cp-kafka-connect-base

### URL
http://localhost:8083/connectors?expand=info&expand=status

## MySQL

Sample MySQL instance for local testing purposes.
Startup scripts are in the `data/mysql` directory.

## CURL

Helper container to configure the Debezium connector through the REST API.
Waits until the Connect cluster is ready, and then PUTs the config in `config/debezium-config-PUT.json`

## KafkaCat

Helper container to act as a consumer or producer for topics.

### Image
https://hub.docker.com/r/confluentinc/cp-kafkacat
