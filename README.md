# api-kafka-flink-influx-grafana

## Goal is to do the following:

- Create a docker compose file to create the following:

  - api conatiner
  - kafka w/ zookeeper
  - flink (job / task managers)
  - influxdb
  - grafana

- Create code to do the following:
  - api that writes to kafka
  - flink job that reads from source of kafka topic inbound, aggregates temp data for 5 minutes, and writes to sink of kafka topic outbound
  - flink job that reads from source of kafka topic outbound and writes to influxdb
  - grafana query that visualizes data written to influxdb
