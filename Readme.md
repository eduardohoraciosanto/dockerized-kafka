# Basic Kafka Setup

## Boot up
Just run `docker-compose up` and both zookeeper and kafka will boot up.
Add `-d` option if you don't want to see the logs from the services.

## Producing and Consuming Messages
To quickly test the kafka broker, use the following commands:

```
To Produce:
kafka-console-producer --topic orders --bootstrap-server broker:9092

To Consume:
kafka-console-consumer --topic orders --bootstrap-server broker:9092
```

Notice that these must be run inside the `broker` service.  
You can get inside the service issuing `docker exec -it {container_id} bash`.  
To get the `container_id` you need to see it using the `docker ps` command.

### More information
Information to create this was taken from https://developer.confluent.io/tutorials