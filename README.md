# kafka-installation-individual

## Commands

- Start the Zookeeper service
```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties ```

- Start the kafka service
``` .\bin\windows\kafka-server-start.bat .\config\server.properties ```

- Create a unique topic
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic hadoopbigdata```

- List all created topics 
``` .\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list ```

- Start a Kafka producer for writing messages
``` .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic hadoopbigdata ```

- Start a Kafka consumer for retrieving messages 
``` .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic hadoopbigdata --from-beginning```
