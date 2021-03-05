# db

## Database
**Database** is a convinient way to structure and store information efficiently (e.g. in tables). A **relational database** uses keys to link pieces of data from one table to another, whereas each **key** represents some relation (e.g. a unique identifier of an owner). **SQL (structured query language)** is a query language used to access and manage data in the relational database. There are also **NoSQL (not only SQL)** databases, which can exploit storage resources and structural integrity in exchange for better performance.

Three types of relationship are possible between two tables in a simple relational database:
- **one-to-one**,
- **one-to-many**,
- **many-to-many**.

## One-to-one relationship
It's a situation when one record in a table corresponds to only one record in another table. For example, each country has one unique capital; therefore there could be two tables that must be linked: countries and cities. In such a situation two tables can be represented as one bigger table with additioinal fields, but separating information onto two tables may be useful for following reasons:
- Performance and efficiency, especially if fields in one table are empty sometime;
- Clear semantics, if one table represents some entity or member of a class;
- Design choice, for it's easier to manage separate tables for utility and security.

## One-to-many relationship
When one record in a table corresponds to many records in another table, and not other way around. For example, each customer has one or more orders; since any order is unique and must be linked to only one customer, and each customer might make a few such orders, the database can be implemented as two related tables: customers and orders. The relationship **many-to-one** is a matter of perspective, and is technically equivalent.

## Many-to-many relationship
When one record in a table corresponds to many records in another table, and one record in the other table corresponds to many records in the first. For example, each book assigned many genres (tags), and each genre assigned many books. Such a database can be implemented in many ways:
- With the help of **junction table**;
- Via encoding categories into separate fields.

## A list of open-source databases:
- **MySQL** - one of the most popular choices for data organization and storage;
- **PostgreSQL** - has advanced level of complexity, array data type, support for python scripts;
- **MongoDB** - stores similar data in chunks;
- **Redis** - great for caching, data lives entirely in RAM;
- **SQLite** - a portable solution without need for setting up a server;
- **Cassandra** - uses columns of data instead of rows, good write speed;
- **MariaDB** - a MySQL close alternative, absolutely free;
- **Neo4j** - for graphs and networks.
