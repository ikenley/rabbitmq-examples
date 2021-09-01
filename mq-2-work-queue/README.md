# mq-2-work-queue

[Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-java.html)

```
mvn package

# shell 1
java -cp ./target/rabbitmq-work-queue-1.0-SNAPSHOT.jar com.ikenley.rabbitmqworkqueue.Worker

# shell 2
java -cp ./target/rabbitmq-work-queue-1.0-SNAPSHOT.jar com.ikenley.rabbitmqworkqueue.Worker

# shell 3
java -cp ./target/rabbitmq-work-queue-1.0-SNAPSHOT.jar NewTask First message.
java -cp ./target/rabbitmq-work-queue-1.0-SNAPSHOT.jar NewTask Second message..
java -cp ./target/rabbitmq-work-queue-1.0-SNAPSHOT.jar NewTask Third message...
java -cp ./target/rabbitmq-work-queue-1.0-SNAPSHOT.jar NewTask Fourth message....
java -cp ./target/rabbitmq-work-queue-1.0-SNAPSHOT.jar NewTask Fifth message.....

java -cp ./target/rabbitmq-work-queue-1.0-SNAPSHOT.jar com.ikenley.rabbitmqworkqueue.NewTask
```
