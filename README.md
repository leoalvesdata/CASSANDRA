Apache Cassandra Course Platform Database

This project demonstrates the development of a NoSQL data model using Apache Cassandra and CQL (Cassandra Query Language) for an online course platform.

The main goal was to design a scalable and flexible database structure capable of storing information about platform members and available courses while applying core Cassandra concepts such as partition keys, clustering columns, static columns, collections, and secondary indexes.

The proposed problem involved creating a database model that could:

Store member information
Store course information
Support efficient course searches
Allow schema evolution
Perform CRUD operations in a distributed NoSQL environment

To solve this, a keyspace called tokio was created along with two main tables:

membro → stores user data
cursos → stores course data

Some important modeling decisions were implemented during development:

The tipo column was defined as a STATIC column to avoid redundant data storage inside partitions.
The professor field was modeled using a map structure to store both the instructor’s name and email.
A new interesses column was later added using a list collection type, demonstrating Cassandra schema evolution capabilities.
A secondary index was created for the categoria column to allow filtering courses by category.

The project also includes practical examples of:

Data insertion
Data querying
Record updates
Record deletion
Table documentation using comments

Additionally, the implementation demonstrates how Cassandra handles non-relational modeling approaches focused on query efficiency and scalability instead of normalization.

Technologies Used
Apache Cassandra
CQL (Cassandra Query Language)
NoSQL Databases
Main Concepts Applied
Keyspaces
Primary Keys
Partition Keys
Clustering Columns
Static Columns
Collection Types (list)
Map Types (map)
Secondary Indexes
CRUD Operations
Schema Evolution

Based on the exercises proposed in the Tokio School Big Data module.
