# 0x01-NoSQL

This repository contains solutions and projects related to backend storage systems, focusing on NoSQL databases, specifically MongoDB. This repository is part of the ALX Backend program.

## Table of Contents

- [0x01-NoSQL](#0x01-nosql)
  - [Table of Contents](#table-of-contents)
  - [General Information](#general-information)
  - [Resources](#resources)
  - [Learning Objectives](#learning-objectives)
  - [Requirements](#requirements)
    - [MongoDB Command File](#mongodb-command-file)
    - [Python Scripts](#python-scripts)
    - [Installation Instructions](#installation-instructions)
  - [Project Structure](#project-structure)
  - [Tasks](#tasks)
    - [0. List all databases](#0-list-all-databases)
    - [1. Create a database](#1-create-a-database)
    - [2. Insert document](#2-insert-document)
    - [3. All documents](#3-all-documents)
    - [4. All matches](#4-all-matches)
    - [5. Count](#5-count)
    - [6. Update](#6-update)
    - [7. Delete by match](#7-delete-by-match)
    - [8. List all documents in Python](#8-list-all-documents-in-python)
    - [9. Insert a document in Python](#9-insert-a-document-in-python)
    - [10. Change school topics](#10-change-school-topics)
    - [11. Where can I learn Python?](#11-where-can-i-learn-python)
    - [12. Log stats](#12-log-stats)
    - [13. Regex filter](#13-regex-filter)
    - [14. Top students](#14-top-students)
  - [Acknowledgments](#acknowledgments)

## General Information

**Project Name:** 0x01. NoSQL  
**Topic:** Back-end, NoSQL, MongoDB  
**Weight:** 1  
**Start Date:** June 14, 2024  
**End Date:** June 20, 2024  
**Checker Release Date:** June 15, 2024  
**Auto Review:** At the deadline

## Resources

- [NoSQL Databases Explained](https://www.youtube.com/watch?v=1J9TgTLp5Y4)
- [What is NoSQL?](https://www.mongodb.com/nosql-explained)
- [MongoDB with Python Crash Course - Tutorial for Beginners](https://www.youtube.com/watch?v=E-1xI85Zog8)
- [MongoDB Tutorial 2: Insert, Update, Remove, Query](https://www.youtube.com/watch?v=EAE3ljmjdUk)
- [Aggregation](https://docs.mongodb.com/manual/aggregation/)
- [Introduction to MongoDB and Python](https://www.youtube.com/watch?v=E-1xI85Zog8)
- [mongo Shell Methods](https://docs.mongodb.com/manual/reference/method/)
- [Mongosh](https://docs.mongodb.com/mongodb-shell/)

## Learning Objectives

By the end of this project, you should be able to:

- Explain what NoSQL means.
- Differentiate between SQL and NoSQL.
- Define ACID properties.
- Describe document storage.
- List types of NoSQL databases.
- Identify benefits of a NoSQL database.
- Query information from a NoSQL database.
- Insert, update, and delete information from a NoSQL database.
- Use MongoDB effectively.

## Requirements

### MongoDB Command File

- All files should be interpreted/compiled on Ubuntu 18.04 LTS using MongoDB version 4.2.
- All files should end with a new line.
- The first line of all files should be a comment: `// my comment`
- A README.md file, at the root of the project folder, is mandatory.
- The length of your files will be tested using `wc`.

### Python Scripts

- All files should be interpreted/compiled on Ubuntu 18.04 LTS using Python3 version 3.7 and PyMongo version 3.10.
- All files should end with a new line.
- The first line of all files should be exactly `#!/usr/bin/env python3`.
- Your code should use the pycodestyle style (version 2.5.*).
- The length of your files will be tested using `wc`.
- All modules should have documentation.
- Your code should not be executed when imported (by using `if __name__ == "__main__":`).

### Installation Instructions

To install MongoDB 4.2 on Ubuntu 18.04, follow these steps:

```sh
$ wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | apt-key add -
$ echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list
$ sudo apt-get update
$ sudo apt-get install -y mongodb-org
$ sudo service mongod start
$ mongo --version
$ pip3 install pymongo
```

## Project Structure

```sh
alx-backend-storage/
├── 0x01-NoSQL/
│   ├── 0-list_databases
│   ├── 1-use_or_create_database
│   ├── 2-insert
│   ├── 3-all
│   ├── 4-match
│   ├── 5-count
│   ├── 6-update
│   ├── 7-delete
│   ├── 8-all.py
│   ├── 9-insert_school.py
│   ├── 10-update_topics.py
│   ├── 11-schools_by_topic.py
│   ├── 12-log_stats.py
│   ├── 100-find
│   ├── 101-students.py
├── README.md
└── requirements.txt
```

## Tasks

### 0. List all databases

Write a script that lists all databases in MongoDB.

**File:** `0-list_databases`  
**Command:**

```sh
$ cat 0-list_databases | mongo
```

### 1. Create a database

Write a script that creates or uses the database `my_db`.

**File:** `1-use_or_create_database`  
**Command:**

```sh
$ cat 1-use_or_create_database | mongo
```

### 2. Insert document

Write a script that inserts a document in the collection `school`. The document must have one attribute `name` with value `Holberton school`.

**File:** `2-insert`  
**Command:**

```sh
$ cat 2-insert | mongo my_db
```

### 3. All documents

Write a script that lists all documents in the collection `school`.

**File:** `3-all`  
**Command:**

```sh
$ cat 3-all | mongo my_db
```

### 4. All matches

Write a script that lists all documents with `name="Holberton school"` in the collection `school`.

**File:** `4-match`  
**Command:**

```sh
$ cat 4-match | mongo my_db
```

### 5. Count

Write a script that displays the number of documents in the collection `school`.

**File:** `5-count`  
**Command:**

```sh
$ cat 5-count | mongo my_db
```

### 6. Update

Write a script that adds a new attribute to a document in the collection `school`. The script should update only documents with `name="Holberton school"` by adding the attribute `address` with the value `972 Mission street`.

**File:** `6-update`  
**Command:**

```sh
$ cat 6-update | mongo my_db
```

### 7. Delete by match

Write a script that deletes all documents with `name="Holberton school"` in the collection `school`.

**File:** `7-delete`  
**Command:**

```sh
$ cat 7-delete | mongo my_db
```

### 8. List all documents in Python

Write a Python function that lists all documents in a collection.

**File:** `8-all.py`  
**Prototype:** `def list_all(mongo_collection):`

### 9. Insert a document in Python

Write a Python function that inserts a new document in a collection based on kwargs.

**File:** `9-insert_school.py`  
**Prototype:** `def insert_school(mongo_collection, **kwargs):`

### 10. Change school topics

Write a Python function that changes all topics of a school document based on the name.

**File:** `10-update_topics.py`  
**Prototype:** `def update_topics(mongo_collection, name, topics):`

### 11. Where can I learn Python?

Write a Python function that returns the list of schools having a specific topic.

**File:** `11-schools_by_topic.py`  
**Prototype:** `def schools_by_topic(mongo_collection, topic):`

### 12. Log stats

Write a Python script that provides some stats about Nginx logs stored in MongoDB.

**File:** `12-log_stats.py`

### 13. Regex filter

Write a script that lists all documents with name starting by Holberton in the collection `school`.

**File:** `100-find`  
**Command:**

```sh
$ cat 100-find | mongo my_db
```

### 14. Top students

Write a Python function that returns all students sorted by average score.

**File:** `101-students.py`  
**Prototype:** `def top_students(mongo_collection):`

## Acknowledgments

- [ALX](https://www.alxafrica.com/) for providing the project guidelines and resources.
