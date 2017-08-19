# nosqldbs

## What's NoSQL

* “No SQL”? 

* “Not Only SQL”?

* Non Relational?

* Schema-less?

---

## CAP Theorem

From Wikipedia, the free encyclopedia

It is impossible for a distributed data store to simultaneously provide more than two out of the following three guarantees

| Consistency       | Availability           | Partition Tolerance  |
| ----------------- |:----------------------:| --------------------:|
| Every read receives the most recent write or an error      | Every request receives a (non-error) response – without guarantee that it contains the most recent write |The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes |


Since network partition is usually given in a distributed system, it's pretty much:
			
Consistency vs. Availability

---

## ACID vs BASE

### ACID Consistency Model
* Atomic, Consistent, Isolated, Durable
* Favors ‘C’ in CAP

### BASE Consistency Model
* Basically Available Eventually Consistent
* Favors ‘A’ in CAP

---

## DB Types

### KeyValue DB
* CRUD operations for a Key, Value
* Examples : Redis, Riak

### Document DB
* JSON/BSON Documents
* Examples: MongoDB, CouchDB

### Column Store DB
* Data stored with rowkey and column families
* Examples: Hbase, Cassandra

### Graph DB
* Store Entities and Relationships
* Examples: Neo4j, Infinite Graph

---

## Key Value DB (Redis)

* DataStructure Server (Sets, SortedSets, BitMaps, HyperLogLogs, Pub-Sub)

* Serialized Execution of Commands

* In-Memory with Periodic Backup or Append Only File (AoF) Persistence 

---

## Key Value DB (Riak)

Riak Ring Buffer
Based on Amazon’s Dynamo paper http://docs.basho.com/riak/kv/2.2.3/learn/dynamo/

N=Number of replicas

### Eventual Consistency
* R/W = Read/Write Quorom
* R=1  Sloppy quorum, Faster reads, but possibly dirty. Same for W
* Increase R, W values for stronger consistency and partition tolerance
* Controlled at bucket level

* Masterless Architecture
* Data Structures
* Tables ~= Buckets

---

## Document DB (Mongo)

* JSON/Binary JSON (BSON) documents
* Collections ~= Tables
* Indexing
* Queries return cursor

---

## Graph DB (Neo4j)

* Nodes and Relationships
* Cypher Language
* Indexes for Starting Points

---

## Column Store DB (HBase)

* Column-Oriented based on Google’s BigTable
* Built over HDFS (Hadoop Distributed File Ssytem)
* BigData


