# Kafka Docker setup 

- Clone this repository

- Move inside the project and execute the command

```
docker compose up -d

```

- when kafka is started run a command

```
docker exec -it -w /opt/kafka/bin broker sh

```
- I will be in the kafka execution folder

- I have to add topic in kafka

```
./kafka-topics.sh --create --topic sample-topic --bootstrap-server broker:29092

```
- Add another topic

```
./kafka-topics.sh --create --topic user-topic --bootstrap-server broker:29092

```

- To produce data in topic

```
./kafka-console-producer.sh --topic sample-topic --bootstrap-server broker:29092

```

- To consume data from topic

```
./kafka-console-consumer.sh --topic sample-topic --from-beginning --bootstrap-server broker:29092

```
