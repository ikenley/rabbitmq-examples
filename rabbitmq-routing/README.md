# rabbitmq-routing

[Routing](https://www.rabbitmq.com/tutorials/tutorial-four-java.html)

```
# Start RabbitMQ
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.9-management

mvn package

# terminal 1
java -cp ./target/rabbitmq-routing-1.0-SNAPSHOT.jar com.ikenley.rabbitmqrouting.ReceiveLogsDirect warning error

# terminal 2
java -cp ./target/rabbitmq-routing-1.0-SNAPSHOT.jar com.ikenley.rabbitmqrouting.ReceiveLogsDirect info warning error

# terminal 3
java -cp ./target/rabbitmq-routing-1.0-SNAPSHOT.jar com.ikenley.rabbitmqrouting.EmitLogDirect info "Open the pod bay doors, HAL"
java -cp ./target/rabbitmq-routing-1.0-SNAPSHOT.jar com.ikenley.rabbitmqrouting.EmitLogDirect warning "I can't let you do that, Dave"
```
