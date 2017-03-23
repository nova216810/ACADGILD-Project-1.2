# ACADGILD-Project-1.2
Titantic Analysis

The data set contains information about passengers who boarded Titanic ship. It contains data points like:

DATA SET DESCRIPTION
Column 1 : PassengerId
Column 2 : Survived(survived=0 & died=1)
Column 3 : Pclass
Column 4 : Name
Column 5 : Sex
Column 6 : Age
Column 7 : SibSp
Column 8 : Parch
Column 9 : Ticket
Column 10 : Fare
Column 11 : Cabin
Column 12 : Embarked

Problem Statement
-----------------
You can use any of the technologies like Map Reduce, Pig or Hive of your choice.
Note:You need to copy the data set into HDFS using flume and send the screen shot of that with the project solution

Copying Dataset from Local to HDFS through FLUME
------------------------------------------------
1.Create a configuration file to move dataset from local to HDFS : titanic.conf (refer code)

2.Open Terminal 1, and execute the command:
flume-ng agent --conf-file titanic.conf --name titanic --conf $FLUME_HOME/conf -Dflume.root.logger=INFO,console

3.Open Terminal 2 and check if the dataset has been copied to HDFS 
[acadgild@localhost ~]$ hadoop fs -ls /titanicOP
17/03/22 21:36:20 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Found 11 items
-rw-r--r--   1 acadgild supergroup    1769205 2017-03-22 21:31 /titanicOP/FlumeData.1490198481680
-rw-r--r--   1 acadgild supergroup    1699201 2017-03-22 21:31 /titanicOP/FlumeData.1490198481681
-rw-r--r--   1 acadgild supergroup    2732106 2017-03-22 21:31 /titanicOP/FlumeData.1490198481682


