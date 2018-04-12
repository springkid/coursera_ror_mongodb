# Week 1 README
Resumen de las transparencias de la Semana 1.

# Welcome to Module 1: Introduction to MongoDB, Mongo-Ruby API and CRUD.
1. Introduction to NoSQL and MongoDB
2. CRUD operations
3. Integrating Ruby/Rails with MongoDB


## Introduction to NoSQL and MongoDB.

### Welcome to Module 1: Introduction to MongoDB, Mongo-Ruby API and CRUD.

### Github repository for Module 1

[Github repository for Module 1](https://github.com/jhu-ep-coursera/fullstack-course3-module1-zips)

### Introduction to NoSQL and MongoDB (12 min.)

#### Why RDBMS?
- RDBMS: Oracle
- Low cost RDBMS: PostgreSQL, MySQÑ, SQLLite
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

## Categories of NoSQL (8 min)
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
