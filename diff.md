Known issues:
1) 'DataFrame' object has no attribute 'map'
`mydf.map() --> mydf.rdd.map()`

2) When using regression functions from `pyspark.ml.classification` such as `LogisticRegression`, column features of input data must be of type `org.apache.spark.ml.linalg.VectorUDT@3bfc3ba7` instead of  `org.apache.spark.mllib.linalg.VectorUDT@f71b0bce`. 

3) It sometimes throws an error that numpy is required  using Spark with yarn,, but using with local mode has no such problem.
E.g. CS120/lab2 running `df.rdd.map(lambda x: LabeledPoint(x[0].split(",")[0], x[0].split(",")[1:])).toDF()` on Spark yarn will get an error that numpy is required.
