# RecommendationSystem

## Change Log 
* 8/Apr: Update the word_cloud.ipynb - Have a fun with WordCloud library.

## Configuration 

```
docker run -it --rm -p 8888:8888 -v <your_local_path>:/home/jovyan/work jupyter/pyspark-notebook
```

Testing code 

```
import pyspark 
sc = pyspark.SparkContext('local[*]')
# do something to prove it works
rdd = sc.parallelize(range(1000))
rdd.takeSample(False, 5)
```
