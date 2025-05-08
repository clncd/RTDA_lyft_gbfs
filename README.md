# RTDA_lyft_gbfs

## Environment

We are using <https://github.com/sebkaz/jupyterlab-project> provided by [sebastianzajac.pl](https://sebastianzajac.pl).

## Producer Instructions

1. Launch jupyterlab-project and access the environment (by default `localhost:8888`).
2. Create a kafka topic `kafka/bin/kafka-topics.sh --bootstrap-server broker:9092 --create --topic lyft_station_status`.
3. (Skip this step if you have your own consumer) Launch a simple terminal consumer `kafka/bin/kafka-console-consumer.sh --bootstrap-server broker:9092 --topic lyft_station_status --from-beginning`.
4. Start the producer `python3 GBFS_producer.py`
5. Once you are done you can stop the producer through a keyboard interrupt `^c`.
