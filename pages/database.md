---
title: Database Setup 
layout: page
permalink: /database/
---

## Database

Kereru requires [MySQL](https://www.mysql.com/) or [MariaDB](https://mariadb.org/) to be installed and running.

The database and database user must be created manually before use.

## Setup

From a MySQL shell

```console
# mysql -u root -p
```

The following SQL will a database called <tt>kereru</tt>, a databse user called <tt>twitter</tt> with a password of <tt>insecure</tt>:

```mysql
CREATE DATABASE IF NOT EXISTS kereru;
CREATE USER IF NOT EXISTS 'twitter'@'localhost' IDENTIFIED BY 'insecure';
GRANT ALL PRIVILEGES ON kereru . * TO 'twitter'@'localhost';
FLUSH PRIVILEGES;
```

The example above is a guide to setting up the database in one particular way, and assumes a default configuration for a new database server. You may want to read the official [MariaDB](https://mariadb.com/kb/en/create-user/) or [MySQL](https://dev.mysql.com/doc/refman/en/create-user.html) documentation for more detail.
