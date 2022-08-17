# Data-collection-and-analysis-platform-for-Internet-of-vehicles
MQTT+Kafka+KSQL+Tensorflow

## After building each configuration software, the required code is in the `code` file.

[1] `mqtt_client` contains car sensor simulation data files and MQTT client build code.
`mqtt_client.py` implements the creation of three MQTT clients, reads the `sensor_data-Copy1.csv` file, and sends data to the MQTT Broker.

[2] `DataProcess` contains code for obtaining data from Kafka to local, converting data file format, and data processing to build model prediction.

* First, use `kafka-consumer.py` to get data from Kafka and save it to `data-sensor.txt` file.
* Then, use `txt2csv.py` to convert the data to `.csv` format, where if the transmitted data is in a non-dictionary format, use #not dict. If the transferred data is in dictionary format, use #dict.
* Finally, use `ipython-lstm-train.ipynb` to perform data analysis, build models, and predict data.
