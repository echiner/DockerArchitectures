# DockerArchitectures
Basic Docker configurations to test different architectures easily.

## Architectures

The following architectures are defined in docker-compose:

|  Name  | File   | Description  | Components |
| :------------ | :------------ | :------------ | :------------ |
|   CDC Kafka |  mysql-cdc-kafka.yml |  CDC-like using Kafka Connect (JDBC)  | MySQL, Adminer DB Manager, and Full Kafka Stack |
|  Metabase | mysql-metabase.yml  | Metabase installation with MySQL as storage  | MySQL, Adminer DB Manager, and Metabase |
| Prometheus/Grafana | prometheus-grafana.yml | Test Prometheus/Grafana architecture agains docker monitor | Prometheus (with Alert Manager and Node Exporter), Grafana and cAdvisor |

## Running

### Setup and tear down

Run the following command to **setup the infrastructure**:
```
docker-compose -f config/<archiecture-file>.yml up -d
```

Run the following command to **teardown the infrastructure**:
```
docker-compose -f config/<archiecture-file>.yml up -d
```

### Starting & stopping specific components
Starting:
```
docker-compose -f config/<archiecture-file>.yml start <service_name>
```

Stopping:
```
docker-compose -f config/<archiecture-file>.yml stop <service_name>
```