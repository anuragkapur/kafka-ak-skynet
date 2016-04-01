## Introduction

Kafka is a distributed, partitioned, replicated commit log service. It provides the functionality of a messaging system,
 but with a unique design
 
### Terminology
 * Topics - category for a feed of messages
 * Producers - processes that publish messages to kafka
 * Consumers - processes that consume messages from kafka
 * Brokers - individual servers that make up a kafka cluster
 
### Anatomy of a Topic
 * Topics are partitioned
 * Each partition is an ordered, immutable sequence of messages, i.e. a commit log
 * Each message in a partition is assigned a sequentialId called __offset__ - a unique identifier per partition
 * Messages are retained for a configurable period of time
 
## References
* [Official Apache Kafka documentation](http://kafka.apache.org/documentation.html)