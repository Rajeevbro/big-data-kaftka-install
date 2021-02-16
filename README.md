# Helpful commands for Kaftka!

Run the following commands in your Kaftka folder in ur c drive homie:

Start the zookeeper:
```Bash
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```

**NEW WINDOW**

Start the Kaftka:
```Bash
.\bin\windows\kafka-server-start.bat .\config\server.properties
```

**NEW WINDOW**
These are one-time commands. Used to create a topic and list out the new and past topics:
```Bash
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic tasty-noodles
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```

**NEW WINDOW**
To get the prompt to start sending messages, run the following command:
```Bash
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic tasty-noodles
```

**NEW WINDOW**
Wanna see all the messages sent? Run this:
```Bash
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic tasty-noodles --from-beginning
```

Hopefully it all works, because we were lucky to get it working the first time...
