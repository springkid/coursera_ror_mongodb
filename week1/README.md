# Week 1 README
Resumen de las transparencias de la Semana 1.

# Welcome to Module 1: Introduction to MongoDB, Mongo-Ruby API and CRUD.
1. Introduction to NoSQL and MongoDB
2. CRUD operations
3. Integrating Ruby/Rails with MongoDB

---
## Lesson 01. Welcome to Ruby on Rails Web Services and Integration with mongoDB.

---

## Lesson 02. Introduction to NoSQL and MongoDB.

### Welcome to Module 1: Introduction to MongoDB, Mongo-Ruby API and CRUD. (3 min.)

### Github repository for Module 1

[Github repository for Module 1](https://github.com/jhu-ep-coursera/fullstack-course3-module1-zips)

### Introduction to NoSQL and MongoDB (12 min.)

#### Why RDBMS?
- RDBMS: Oracle
- Low cost RDBMS: PostgreSQL, MySQL, SQLLite
- Transsactional
- Supports Joins

#### Why NoSQL ?
- Explosion in data (Unstructured data).
- Object / Relational impedance mismatch: objects are constantle being moved.
- RDBMS joins and normalization are powerful but add up in cost.
- "Big data" handling with better perfomance.
- Supports unstructured data: unique data type can be easily integrated into existing collections.
- Operational issues (scale, performance and availability).

#### Scaling Out
Vertical scaling
Horizontal scaling

#### What is NoSQL
Not Only SQL
No fixed schema
Non-relational data storage systems
redis, couchbase, MongoDB, cassandra, amazon dynamoDB, apache ubase, memcached

#### Summary
Very popular and major companies use it, specially social networking sites (Twitter, FB, LinkedIn, Digg).
Excellent performance and stability, fat and scalable and fairly simple model.
Supports unstructured format => very agile and adaptable.

### Categories of NoSQL (8 min)
#### Categories of NoSQL - Key / Value
Value can be String or JSON.
Infor is stored in Key-value hash.
Dynamo, Redis, Memcached.

#### Categories of NoSQL - Document
Stores documents based up of tagged elements.
Pesistent and query-able.
MongoDB, CouchDB.

#### Categories of NoSQL - Column
Flat structure, but with keys stored in columns rather than rows.
Casandra, Hbase

#### Categories of NoSQL - Graph
A network database that uses edges and nodes to represent and store data.
Neo4J.

#### NoSQL - Not supported
Joins are not supported.
ACID transactions supported at document level only.

#### NoSQL vs RDBMS - How to pick?
Nature of data
- Row or column (Structured) => RDBMS
- Unstructured, complex data (geo spatial or engineering data) that needs nesting => NoSQL

Schema
- Static => RDBMS
- Dynamic => NoSQL

Self-contained => NoSQL, Joins => RDBMS

Flexibility of query : RDBMS Joins allow for flexibility

Cons of NoSQL : duplication of data, implement joins in middle-ware

### Introduction to NoSQL and MongoDB (8 min)
#### What is MongoDB.
Open source, document oriented database, designed with scalability and developer agility in mind.

JSON-like docuemtns and schemaless. BSON

Well suited for OO programming.

#### Document Store (Mapping)
- Database -- Database
- Table, View -- Collection
- Rows -- JSON documents
- Column -- Field
- Index -- Index
- Join -- Embedded document/ Linking across Document
- Foreign key -- Reference
- Partition Key -- Shard

#### Sample Query - SQL vs. Mongo
CREATE TABLE -- insert()
SELECT -- find()
UPDATE -- update()
DELETE -- remove()

#### Why MongoDB
Queryable documents

No impedance mismatch

Quick and easy integration of new data variations

Rich API support (multiple languages)

#### Ruby on Rails & Mongo
Ruby driver
Mongoid

#### MongoDB users

#### MongoDB core topics with Ruby/Rails

MongoDB Ruby driver

Aggregation framework

GridFS: breaking large files into smaller chunks

Geospatial: index and query geospatial data

Mongoid


### MongoDB installation (9 min)

#### MongoDB installation steps

Step 1 : download

Step 2 : default data folder (p.e. /data/db or C:\data\db)

#### Starting MongoDB

#### Launching MongoDB shell

Para más detalle, consultar la documentación de instalación de MongoDB ...

### MongoDB basics (13 min)

#### Importing sample data

mongoimport

zips.JSON

#### Basics of MongoDB shell

Database, Documents and Collections.

#### MongoDB collections

Collection types
- Capped collections
-

#### IRB shell and MongoDB

mongo-ruby driver

### Basic MongoDB commands in IRB

Launch irb console

```
#disable logging
require 'mongo'
Mongo::Logger.logger.level = ::Logger::INFO

#get a connection
db = Mongo::Client.new('mongodb://localhost:27017')

#use test
db=db.use('test')

#database name
db.database.name

# List collections
db.database.collections  OR
db.database.collection_names

# Find first
db[:zips].find.first
```

### Practice Programming Assignment. MongoDB ruby driver connection.

---

## Lesson 3. CRUD

### Inserting documents (5 min)

insert_one
insert_many

```
db[:zips].insert_one(:_id => "100", :city => "city01",
:loc => [-76.05927000, 2.04050607],
:pop => 4678, :state => "MD")

```

```

db[:zips].insert_many([
  {:_id => "200", :city => "city02",
    :loc => [-74.05922700000001, 37.564894 ],
    :pop => 2000, :state => "CA" },
    {:_id => "201", :city => "city03",
      :loc => [-75.09322700000001, 35.564894 ],
      :pop => 3000, :state => "CA" },    
  ])

```

```
db[:zips].find(:city => "city02").to_a

```

### Practice Prograaming Assignment - MongoDB Ruby Driver CRUD (10 min)


### Find (10 min)

### Paging (5 min)


### Advanced find (12 min)

less_than and great less_than

$lt

$gt

```
db[:zips].find()

```
Evaluations
Find By - Regex
$Regex
$exists
$not
$type
