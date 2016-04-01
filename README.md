Kafka Installation on ak-skynet
===============================

## What is this?
This repo houses the kafka setup on my development machine. I like version controlling __everything__!

## Commands

### Starting the server

#### Zookeper
    {kafka_home}/bin/zookeeper-server-start.sh config/zookeeper.properties

#### Kafka
    {kafka_home}/bin/kafka-server-start.sh config/server.properties

### List all topics
    {kafka_home}/bin/kafka-topics.sh --list --zookeeper localhost:2181

### Tail messages in a topic
    {kafka_home}/bin/kafka-console-consumer.sh --zookeeper {zookeeper_hostname}:2181 --from-beginning --topic {topic_name}    
    
## Utilities

### Delete a topic without worrying about the data that may already be there

* Stop Kafka
* Clear out appropriate files in the logs dir as specified by the `logs.dir` attribute in `config/the server.properties`
file