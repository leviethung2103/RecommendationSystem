# RecommendationSystem

## Change Log 
* 8/Apr: Update the word_cloud.ipynb - Have a fun with WordCloud library.

## Configuration 

```
docker run -itd -p 8888:8888 -v /home/hunglv/Downloads/Server_Beauty:/home/jovyan jupyter/pyspark-notebook
```

Testing code 

```
import pyspark 
sc = pyspark.SparkContext('local[*]')
# do something to prove it works
rdd = sc.parallelize(range(1000))
rdd.takeSample(False, 5)
```


## Pyspark and Elastic Search
Be careful when installing the Spark 
Requirements 
* Java version: 8 
* Elastic search: 7.6.2 
* Spark version: 2.4.5
How to download packages and install: https://github.com/IBM/elasticsearch-spark-recommender

Run the command to run the jupyter notebook:
```bash
PYSPARK_DRIVER_PYTHON="jupyter" PYSPARK_DRIVER_PYTHON_OPTS="notebook" /home/hunglv/Downloads/Server_Beauty/spark-docker/spark-2.4.5-bin-hadoop2.7/bin/pyspark --driver-memory 4g --driver-class-path /home/hunglv/Downloads/Server_Beauty/spark-docker/elasticsearch-hadoop-7.6.2/dist/elasticsearch-spark-20_2.11-7.6.2.jar
```
Run the notebook with public IP 
-> Remember to set the driver memory 15G
```bash
PYSPARK_DRIVER_PYTHON="jupyter" PYSPARK_DRIVER_PYTHON_OPTS="notebook --no-browser --port=8889 --ip=0.0.0.0" /data_vol/erv-hunglv/spark_docker/spark-2.4.5-bin-hadoop2.7/bin/pyspark --driver-memory 15g --driver-class-path /data_vol/erv-hunglv/spark_docker/elasticsearch-hadoop-7.6.2/dist/elasticsearch-spark-20_2.11-7.6.2.jar
```

## Install Java 
The Spark version 2.4 requires the Java version 8. 

Check the version of Java
```bash
java -version
```

```bash
sudo apt install openjdk-8-jdk
```

Update the default java environment 
Ref: https://computingforgeeks.com/how-to-set-default-java-version-on-ubuntu-debian/
```bash
sudo update-java-alternatives --list
```
