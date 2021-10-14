# Data-Modeling-with-Apache-Cassandra
Project: Data Modeling with Apache Cassandra
## Primary Key and composite key
https://www.bmc.com/blogs/cassandra-clustering-columns-partition-composite-key/

If those fields are wrapped in parentheses then the partition key is composite. Otherwise the first field is the partition key. Any fields listed after the partition key are called clustering columns. By definition the primary key must be unique. That includes clustering columns, since they are part of the primary key. 

Some examples of primary key definition are:

PRIMARY KEY (a): a is the single partition key and there are no clustering columns

PRIMARY KEY (a, b, c) : a is the single partition key and b and c are the clustering columns

PRIMARY KEY ((a, b), c) : a and b compose the composite partition key and c is the clustering columns.


partition key：意指該筆資料被雜湊(hash)計算後存放位置的依據，相同的partition key值會被存放在相同partiton的位置，也是日後查詢條件的依據。
               partition key也可以是複合的key，宣告時再以小括弧區分，例如PRIMARY KEY((a, b) c)寫法。

cluster columns：宣告主鍵時排在partition key之後的各個欄位都是cluster columns，
                 是用來排序每筆存放資料的順序依據。

Where ：必須包含所有的 partition key 。
