# Data-Modeling-with-Apache-Cassandra
Project: Data Modeling with Apache Cassandra
## Primary Key and composite key
https://www.bmc.com/blogs/cassandra-clustering-columns-partition-composite-key/

If those fields are wrapped in parentheses then the partition key is composite. Otherwise the first field is the partition key. Any fields listed after the partition key are called clustering columns. By definition the primary key must be unique. That includes clustering columns. Clustering columns determines the order of data in partitions. since they are part of the primary key. 

Some examples of primary key definition are:

PRIMARY KEY (a): a is the single partition key and there are no clustering columns

PRIMARY KEY (a, b, c) : a is the single partition key and b and c are the clustering columns

PRIMARY KEY ((a, b), c) : a and b compose the composite partition key and c is the clustering columns. 

Where ：must included all of partition key 。
