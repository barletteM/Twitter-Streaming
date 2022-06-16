## Deployment

My local deployment is done through this [docker-compose.yaml](docker-compose.yaml) file.


### Requirements

- After obtaining your set of Twitter API key and secret, you have to set those in the [secret.ini](./produce-tweets/secret.ini) file.

- Run the Jupyter Notebook [twitstream.ipynb](./model/twitstream.ipynb) to build a model and save it in a *.pickle* file. See the (README.md)[./model/README.md] file for running instructions.

### Starting the Services

Services need to be started in a specific order with the following commands:
```
# Start Kafka and InfluxDB
docker-compose up -d kafka influxdb

# Start Grafana
docker-compose up -d grafana

# Start the producer and the consumer
docker-compose up -d producer consumer
```

```
