# rabbitmq-publish-subscribe

[Publish/Subscribe](https://www.rabbitmq.com/tutorials/tutorial-three-java.html)

```
# Start RabbitMQ
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.9-management

mvn package

# terminal 1
java -cp ./target/rabbitmq-publish-subscribe-1.0-SNAPSHOT.jar com.ikenley.rabbitmqpublishsubscribe.EmitLog

# terminal 2
java -cp ./target/rabbitmq-publish-subscribe-1.0-SNAPSHOT.jar com.ikenley.rabbitmqpublishsubscribe.ReceiveLogs

# terminal 3
java -cp ./target/rabbitmq-publish-subscribe-1.0-SNAPSHOT.jar com.ikenley.rabbitmqpublishsubscribe.ReceiveLogs
```
