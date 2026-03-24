# NoSQL Multi Database Setup with Docker

## Project Overview

This project demonstrates the installation and usage of multiple NoSQL databases using Docker and Docker Compose. The goal is to explore different NoSQL data models and perform basic CRUD operations on each system.

The following databases are included:

* **MongoDB** → Document-based database
* **Cassandra** → Column-based database
* **Neo4j** → Graph-based database
* **Riak KV** → Key-Value database

Each database runs in an isolated Docker container.

---

## Technologies Used

* Docker & Docker Compose
* Ubuntu 24.04 LTS (VirtualBox)
* NoSQL Databases

---

## Project Structure

```
nosql-multi-database-docker/
│
├── cassandra/
│   └── docker-compose.yml
│
├── mongodb/
│   └── docker-compose.yml
│
├── neo4j/
│   └── docker-compose.yml
│
├── riak/
│   └── docker-compose.yml
│
└── README.md
```

---

## How to Run

Each database is managed separately via Docker Compose.

### 🔹 MongoDB

```bash
cd mongodb
docker-compose up -d
```

### 🔹 Cassandra

```bash
cd cassandra
docker-compose up -d
```

### 🔹 Neo4j

```bash
cd neo4j
docker-compose up -d
```

### 🔹 Riak KV

```bash
cd riak
docker-compose up -d
```

---

## Default Ports

| Database  | Port(s)    |
| --------- | ---------- |
| MongoDB   | 27017      |
| Cassandra | 9042       |
| Neo4j     | 7474, 7687 |
| Riak KV   | 8098, 8087 |

---

## Default Credentials

### Neo4j

* **Username:** neo4j
* **Password:** test1234

You can change credentials in the `docker-compose.yml` file.

---

## CRUD Operations

Basic CRUD operations were tested for each database:

### MongoDB

* insertOne()
* find()
* updateOne()
* deleteOne()

### Cassandra

* INSERT
* SELECT
* UPDATE
* DELETE

### Neo4j (Cypher)

* CREATE
* MATCH
* SET
* DELETE

### Riak KV (HTTP API)

* PUT
* GET
* DELETE

---

## Notes

* MongoDB is configured with replica set parameters, but initialization may require:

```bash
rs.initiate()
```

* Cassandra may take some time to fully start on first run.

---

## Project Report

A detailed report explaining the setup, architecture, and CRUD operations is included in this repository.

---

## Purpose of the Project

The main objective of this project is to:

* Understand different NoSQL database models
* Learn Docker-based database deployment
* Compare multiple NoSQL systems in practice
* Perform basic database operations across different architectures

---

## Conclusion

This project successfully demonstrates the setup and usage of four different NoSQL database systems using Docker. Each system was tested with CRUD operations, highlighting the differences between various NoSQL data models.

---

## Author

**Eda Akkuş**
Software Engineering Student

---
