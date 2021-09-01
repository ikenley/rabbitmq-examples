# rabbit-mq-1-hello-world

---

[Downloading and Installing RabbitMQ](https://www.rabbitmq.com/download.html)

```
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.9-management

# http://localhost:15672/#/
# guest:guest

# create project
mvn archetype:generate -DgroupId=com.ikenley.rabbitmq.producer -DartifactId=producer -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```
