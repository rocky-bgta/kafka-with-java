# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/3.3.0/maven-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/3.3.0/maven-plugin/reference/html/#build-image)
* [Spring for Apache Kafka](https://docs.spring.io/spring-boot/docs/3.3.0/reference/htmlsingle/index.html#messaging.kafka)
* [Spring Web](https://docs.spring.io/spring-boot/docs/3.3.0/reference/htmlsingle/index.html#web)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)

### Maven Parent overrides

Due to Maven's design, elements are inherited from the parent POM to the project POM.
While most of the inheritance is fine, it also inherits unwanted elements like `<license>` and `<developers>` from the parent.
To prevent this, the project POM contains empty overrides for these elements.
If you manually switch to a different parent and actually want the inheritance, you need to remove those overrides.

1. Start Zookeeper Server
   For Windows:
   C:\kafka_2.12-3.5.0\bin\windows>zookeeper-server-start.bat C:\kafka_2.12-3.5.0\config\zookeeper.properties

For Linux/Mac
sh bin/zookeeper-server.sh config/zookeeper.properties

2. Start Kafka server/Broker
   For Windows:
   C:\kafka_2.12-3.5.0\bin\windows>kafka-server-start.bat C:\kafka_2.12-3.5.0\config\server.properties

For Linux/Mac
sh bin/kafka-server-start.sh config/server.properties

3. Create topic
   For Windows:
   C:\kafka_2.12-3.5.0\bin\windows>kafka-topics.bat --bootstrap-server localhost:9092 --create --topic NewTopic --partitions 3 --replication-factor 1

For Linux/Mac
sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic NewTopic --partitions 3 --replication-factor 1

4. List out all topic names
   For Windows:
   C:\kafka_2.12-3.5.0\bin\windows>kafka-topics.bat --bootstrap-server localhost:9092 --list

For Linux/Mac
sh bin/kafke-topics.sh --bootstrap-server localhost:9092 --list

5. Describe topics
   For Windows:
   C:\kafka_2.12-3.5.0\bin\windows>kafka-topics.bat --bootstrap-server localhost:9092 --describe --topic NewTopic

For Linux/Mac
sh bin/kafka-topics --bootstrap-server localhost:9092 --describe --topic NewTopic

6. Produce message

For Windows:
C:\kafka_2.12-3.5.0\bin\windows>kafka-console-producer.bat --broker-list localhost:9092 --topic NewTopic

For Linux/Mac
sh bin/kafka-console-producer.sh --broker-list localhost:9092 --topic NewTopic

7. Consume message
   For Windows:
   C:\kafka_2.12-3.5.0\bin\windows>kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic NewTopic --from-beginning

For Linux/Mac
sh bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic NewTopic --from-beginning




