kaggle project using spark

git clone git://github.com/apache/spark.git 

build spark from git:

export MAVEN_OPTS="-Xmx512m -XX:MaxPermSize=128m"
dev/change-version-to-2.11.sh
mvn -Pyarn -Phadoop-2.4 -Dscala-2.11 -DskipTests clean package

Spring tool suit supports scala


http://spark.apache.org/docs/latest/quick-start.html
Use sbt to package spark scala:
see sample

need to install sbt, 
$ brew install sbt 
on mac
$ sbt package

# Use spark-submit to run your application
$ YOUR_SPARK_HOME/bin/spark-submit \
  --class "SimpleApp" \
  --master local[4] \
  target/scala-2.10/simple-project_2.10-1.0.jar


use titanic data on 
https://www.kaggle.com/c/titanic/details/getting-started-with-python
try the tutorial first, using python

install Anaconda as suggested. You can start tools in Anaconda from launcher
run the random forest example as:
/anaconda/bin/python myfirstforest.py
document for random forest algo in scikit:
http://scikit-learn.org/dev/modules/generated/sklearn.ensemble.RandomForestClassifier.html

Explore scala spark, go to your spark git cloned place, run:
spark/bin/spark-shell


You can start a cluster with yarn or mesos, but a simple cluster can be started with standalone mode:
https://spark.apache.org/docs/latest/spark-standalone.html
You can start a master and several workers on your local computer for testing and developing.
