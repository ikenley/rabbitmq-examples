# rabbitmq-topic

[Topics](https://www.rabbitmq.com/tutorials/tutorial-five-java.html)

```
# Start RabbitMQ
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.9-management

mvn package

# To receive all the logs:
java -cp ./target/rabbitmq-topic-1.0-SNAPSHOT.jar com.ikenley.rabbitmqtopics.ReceiveLogsTopic "#"

# To receive all logs from the facility "kern":
java -cp ./target/rabbitmq-topic-1.0-SNAPSHOT.jar com.ikenley.rabbitmqtopics.ReceiveLogsTopic "kern.*"

#Or if you want to hear only about "critical" logs:
java -cp ./target/rabbitmq-topic-1.0-SNAPSHOT.jar com.ikenley.rabbitmqtopics.ReceiveLogsTopic "*.critical"

# You can create multiple bindings:
java -cp ./target/rabbitmq-topic-1.0-SNAPSHOT.jar com.ikenley.rabbitmqtopics.ReceiveLogsTopic "kern.*" "*.critical"

# And to emit a log with a routing key "kern.critical" type:
java -cp ./target/rabbitmq-topic-1.0-SNAPSHOT.jar com.ikenley.rabbitmqtopics.EmitLogTopic "kern.critical" "A critical kernel error"
```
