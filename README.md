# DockerArchitectures
Basic Docker configurations to test different architectures easily.

## Architectures

The following architectures are defined in docker-compose:

|  Name  | Folder   | Description  | Components |
| :------------ | :------------ | :------------ | :------------ |
|   CDC Kafka |  mysql-cdc-kafka |  CDC-like using Kafka Connect (JDBC)  | MySQL, Adminer DB Manager, and Full Kafka Stack |
|  Metabase | mysql-metabase  | Metabase installation with MySQL as storage  | MySQL, Adminer DB Manager, and Metabase |
| Prometheus/Grafana | prometheus-grafana | Test Prometheus/Grafana architecture agains docker monitor | Prometheus (with Alert Manager and Node Exporter), Grafana and cAdvisor |

## Running

### Setup and tear down

Enter the desired architecture folder:
```
cd <architecture-folder>
```

Run the following command to **setup the infrastructure**:
```
docker-compose up -d
```

Run the following command to **teardown the infrastructure**:
```
docker-compose down -d
```

### Starting & stopping specific components

Enter the desired architecture folder:
```
cd <architecture-folder>
```

Starting everything:
```
docker-compose start
```

Starting only a service:
```
docker-compose start <service_name>
```

Stopping everything:
```
docker-compose stop
```

Stopping only a service:
```
docker-compose stop <service_name>
```