All the labs have been tested on PySpark 2.1.0
Reference labs are based on Spark 1.6.1

1) 'DataFrame' object has no attribute 'map'
`mydf.map() --> mydf.rdd.map()`

2) When using regression functions from `pyspark.ml.classification` such as `LogisticRegression`, column features of input data must be of type `org.apache.spark.ml.linalg.VectorUDT@3bfc3ba7` instead of  `org.apache.spark.mllib.linalg.VectorUDT@f71b0bce`. 

3) Some datasets used here can be downloaded from https://github.com/spark-mooc/cs100-data and https://github.com/spark-mooc/cs190-data. Others may be downloaded directly from references mentioned in each lab. To run the labs, upload datasets to cluster manually and edit loading path in each lab respectively.
