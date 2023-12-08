

- kubectl port-forward kafka-broker-79dc798d9-q4vz7 9092 -n kafka
- kubectl exec --stdin --tty kafka-broker-79dc798d9-q4vz7 -n kafka -- /bin/bash
- kafka-topics.sh --create --topic test --partitions 1 --replication-factor 1 --bootstrap-server kafka-broker:9092
- which kafka-console-consumer.sh
- kcat -P -b localhost:9092 -t test -K: -l text.txt
- kcat -C -b localhost:9092 -t test -o beginning
