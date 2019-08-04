# GISTDA (Twitter Scraping Code on Colab)

Date: Tuesday 6, 2019

1. Twitter Search
Code:https://colab.research.google.com/drive/1EjJALkZqU4WvHcUhYddLK-_97sh9_Wys

2. AnalyzeTwitter
Code: https://colab.research.google.com/drive/167glrgTDzak6Nn_U-B6JOX4JImyihzxM

Github: https://github.com/davidjohnnn/gistda



# SPARK Lab and Exercises 
(GISTDA 2019)
http://bit.ly/spark_gistda

## Lecture Slide:

https://drive.google.com/open?id=1IRk4sNCYk6MDDzwnwE_9ZvVCc--D6fnI


## Lecture Code:

1_Pyspark_Transform_Action
https://colab.research.google.com/drive/150MnQ0Fx1-reySAXsQ24L-B-SVu6aPSS

2_Pyspark_Basic_RDD
https://colab.research.google.com/drive/1tT2iADsbFtHrjH2umsGVqLm_fwRjeMUQ

3_Pyspark_Basic_DataFrame
https://colab.research.google.com/drive/1eigU50O5ZeUOvQI4e6AKD3KD-xKK9PaP

4_Pyspark_Classification_Pipeline_Churn
https://colab.research.google.com/drive/1eKnTRYII82z_vVp2L4ZdHCgpLzDuKFBi

5_Pyspark_Clustering_Pipeline_Cdr
https://colab.research.google.com/drive/1V7qOkBGLAUWyW3np2hnrSWDU9PVjm2O1

## Exercises:

0_Titanic_Solution
https://colab.research.google.com/drive/1k0lMxCZhzTHFtOZcWi0aAfIHhowrvtoz

1_DecisionTree_Pipeline_Iris_Solution
https://colab.research.google.com/drive/18tvStCyU0l0oz0b4mTmm1jSHwj-pjsgi

## Installation

### Upload files to Colab
from google.colab import files
uploaded = files.upload()


### Write out files with Colab
from google.colab import files
files.download('data.dat')

### Spark Installation on Colab

!apt-get install openjdk-8-jdk-headless -qq > /dev/null
!wget -q http://www-eu.apache.org/dist/spark/spark-2.4.3/spark-2.4.3-bin-hadoop2.7.tgz
!tar xf spark-2.4.3-bin-hadoop2.7.tgz
!pip install -q findspark

import os
os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-8-openjdk-amd64"
os.environ["SPARK_HOME"] = "/content/spark-2.4.3-bin-hadoop2.7"
import findspark
findspark.init()
from pyspark.sql import SparkSession
spark = SparkSession.builder.master("local[* ]").getOrCreate()

