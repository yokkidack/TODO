
Where relational databases have tables, MongoDB has collections. In other words, MySQL (a popular relational database) keeps its data in tables of rows, while MongoDB keeps its data in collections of documents, which you can think of as a group of documents.
Internally, MongoDB stores documents in a format called Binary JSON, or BSON.
In theory, each document in a collection can have a completely different structure; in practice, a collection’s document will be relatively uniform.

MDB supports Ad hoc queries

MDB allows using up to 64 indexes per collection (as opposed to single primery key in SQL DB)

MongoDB provides database replication via a topology known as a replica set. Replica sets distribute data across two or more machines for redundancy and automate failover in the event of server and network outages. Additionally, replication is used to scale database reads. If you have a read-intensive application, as is commonly the case on the web, it’s possible to spread database reads across machines in the replica set cluster.
Replica sets consist of many MongoDB servers, usu- ally with each server on a separate physical machine; we’ll call these nodes. At any given time, one node serves as the replica set primary node and one or more nodes serve as secondaries. Like the master-slave repli- cation that you may be familiar with from other data- bases, a replica set’s primary node can accept both reads and writes, but the secondary nodes are read- only. What makes replica sets unique is their support for automated failover: if the primary node fails, the cluster will pick a secondary node and automatically promote it to primary. When the former primary comes back online, it’ll do so as a secondary.
