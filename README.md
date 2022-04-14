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
