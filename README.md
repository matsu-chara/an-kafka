centos6.5(kafka)

java, zookeeper, kafkaが入る

## install

```
git clone https://github.com/matsu-chara/an-kafka
cd an-kafka
vagrant up
```

## memo

* インストールの手順は以下を参考にした。 http://kimutansk.hatenablog.com/entry/20130804/1375614109

```
vagrant ssh
cd /opt/kafka
sudo /opt/kafka/bin/kafka-server-start.sh /opt/kafka_config/server.properties
/opt/kafka/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test
/opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --zookeeper localhost:2181 --topic test --from-beginning
```
