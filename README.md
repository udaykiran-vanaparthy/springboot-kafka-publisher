# kafka-publisher
Apache Kafka Publisher Example using SpringBoot

# start zookeeper.start bat file like below
zookeeper-server-start.bat C:\java Material\softwares\kafka_2.12-1.1.0\config\zookeeper.properties

# start kafka server
kafka-server-start.bat C:\java Material\softwares\kafka_2.12-1.1.0\config\server.properties

# Create Topic:
kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 -topic javaMaster

# Produce a message 
kafka-console-producer.bat --broker-list localhost:9092 --topic javaMaster

# Consume a message
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic javaMaster
