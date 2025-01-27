# Setup Apache Kafka locally
docker compose up -d


## Commands

To consume the data in the broker, start with opening up the container interactively with 

```bash
docker exec -it broker /bin/bash
kafka-topics --list --bootstrap-server localhost:9092
exit
```


To see control center in browser
http://localhost:9021/ 


To make venv in windows and run python codes

```bash
python -m venv virtualenv
python .\src\producer.py
```

```bash
docker exec -it broker /bin/bash
kafka-topics --list --bootstrap-server localhost:9092
kafka-topics --describe --topic jokes --bootstrap-server localhost:9092
kafka-console-consumer --bootstrap-server localhost:9092 --topic jokes --from-beginning
```

To run python codes 

```bash
python .\src\producer.py
python .\src\consumer.py
```