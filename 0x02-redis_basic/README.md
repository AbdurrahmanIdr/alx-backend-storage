# Project: Redis Basic Operations

## Introduction

This project aims to demonstrate basic operations with Redis, focusing on caching and storing data using Python. Each task is designed to build upon the previous one, exploring different functionalities of Redis such as storing strings, managing lists, and implementing a simple cache system.

## Requirements

- Ubuntu 18.04 LTS
- Python 3.7
- Redis Server
- Redis Python Client (`redis` package)
- Pycodestyle (version 2.5)

## Setup Instructions

1. Install Redis on Ubuntu 18.04:

   ```bash
   sudo apt-get -y install redis-server
   pip3 install redis
   sed -i "s/bind .*/bind 127.0.0.1/g" /etc/redis/redis.conf
   ```

2. Clone the repository and navigate to the project directory.
3. Ensure all Python files are executable (`chmod +x *.py`).
