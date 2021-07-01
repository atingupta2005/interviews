# SQL Question
- Refer:
	- https://www.interviewbit.com/sql-interview-questions/

- SQL Azure firewall is a security mechanism that blocks requests based on its IP address.

- 150 databases (including master database) can be created in a single SQL Azure server.

- SQL Azure is the cloud-based relational database

- If the SQL Azure database will reach the max size, data read or fetch operations will still work on it but create, insert or update operations will stop with it.

- For process to migrate to SQL Azure from SQL server use the tool named as SQL Azure Migration Wizard for it. we can use BCP or SSIS

- DATA SYNC to sync SQL Azure with on-premise SQL server.

- 3 database replicas are used in SQL Azure for backup.

- Followings are some of the benefits of the sharded database –
		- Allows users to take benefit of maximum resources within the cloud
		- Reduces the chances of a single point of failure
		- Reduces SQL Azure throttling and I/O bottlenecks

- Are you able to choose the version of SQL Server at creation time?
		- Answer:  No. You are given the latest and greatest version of Azure SQL Database at the time of creation, which as of the writing of this post is V12.

- How do I check the performance of my current Databases to determine the amount of DTUs I need?
		- Answer:  The Database Transaction Unit (DTU) Calculator can be used to help you analyze and capture the needed performance metrics from your current server and workload.


- How to add entries to the SQL Database firewall?
		- There are two approaches towards setting firewall rules for SQL Database, either at the server-level or at the database-level. It is better to set the rules as needed at the database-level, but there are cases where it is easier, or necessary, to define the rules at the server-level.

		-SELECT * FROM sys.database_firewall_rules

- OLTP uses traditional DBMS.
- OLAP uses the data warehouse.

- OLTP database must maintain data integrity constraints
- OLAP database does not get frequently modified. Hence, data integrity is not an issue

- Sharding is just another name for "horizontal partitioning" of a database.
		- The word “Shard” means “a small part of a whole“
			- In DBMS, Sharding is a type of DataBase partitioning in which a large DataBase is divided or partitioned into smaller data, also known as shards.
			- With limited CPU, storage capacity, and memory, query throughput and response times are bound to suffer. When it comes to adding resources to support database operations, vertical scaling (aka scaling up) has its own set of limits and eventually reaches a point of diminishing returns.

- Horizontal partitioning involves putting different rows into different tables
- Vertical partitioning involves creating tables with fewer columns and using additional tables to store the remaining columns

	- Hash Sharding
	- Range Sharding

- Different types of Normalization are:

		- First Normal Form (1NF): A relation is said to be in 1NF only when all the entities of the table contain unique or atomic values.
		- Second Normal Form (2NF): A relation is said to be in 2NF only if it is in 1NF and all the non-key attribute of the table is fully dependent on the primary key.
		- Third Normal Form (3NF): A relation is said to be in 3NF only if it is in 2NF and every non-key attribute of the table is not transitively dependent on the primary key.

- What is a join?
	- This is a keyword used to query data from more tables based on the relationship between the fields of the tables


- An Index is a key built from one or more columns in the database that speeds up fetching rows from the table
- There are three types of indexes -.

- Unique Index.
	- This indexing does not allow the field to have duplicate values if the column is unique indexed. Unique index can be applied automatically when primary key is defined.

- Cluster index is a type of index which sorts the data rows in the table on their key values. In the Database, there is only one clustered index per table.

- A Non-clustered index stores the data at one location and indices at another location. The index contains pointers to the location of that data. A single table can have many non-clustered indexes as an index in the non-clustered index is stored in different places.


- ACID (Atomicity, Consistency, Isolation, Durability) is a set of properties that guarantee that database transactions are processed reliabl

- Entity (Noun): An entity can be a real-world object, either tangible or intangible, that can be easily identifiable. For example, in a college database, students, professors, workers, departments, and projects can be referred to as entities. Each entity has some associated properties that provide it an identity.

- Relationships (Verb): Relations or links between entities that have something to do with each other. For example - The employees table in a company's database can be associated with the salary table in the same database.

- The TRUNCATE command is used to delete all the rows from the table and free the space containing the table.
The DELETE command deletes only the rows from the table based on the condition given in the where clause or deletes all the rows from the table if no condition is specified. But it does not free the space containing the table.

- Collation refers to a set of rules that determine how data is sorted and compared. Rules defining the correct character sequence are used to sort the character data.

- A stored procedure is a subroutine available to applications that access a relational database management system

- How to create empty tables with the same structure as another table?
	-	SELECT * INTO Students_copy FROM Students WHERE 1 = 2;

- A checkpoint is like a snapshot of the DBMS state. Using checkpoints, the DBMS can reduce the amount of work to be done during a restart in the event of subsequent crashes. 	Checkpoints are used for the recovery of the database after the system crash.

- A Relation Schema is specified as a set of attributes. It is also known as table schema. It defines what the name of the table is. Relation schema is known as the blueprint with the help of which we can explain that how the data is organized into tables. This blueprint contains no data.


- There are two integrity rules in DBMS:
	- Entity Integrity : It specifies that "Primary key cannot have a NULL value."
	- Referential Integrity: It specifies that "Foreign Key can be either a NULL value or should be the Primary Key value of other relation

- Explain ACID properties
	- ACID properties are some basic rules, which has to be satisfied by every transaction to preserve the integrity. These properties and rules are:

- ATOMICITY: Atomicity is more generally known as ?all or nothing rule.' Which implies all are considered as one unit, and they either run to completion or not executed at all.

- CONSISTENCY: This property refers to the uniformity of the data. Consistency implies that the database is consistent before and after the transaction.

- ISOLATION: This property states that the number of the transaction can be executed concurrently without leading to the inconsistency of the database state.

- DURABILITY: This property ensures that once the transaction is committed it will be stored in the non-volatile memory and system crash can also not affect it anymore.
