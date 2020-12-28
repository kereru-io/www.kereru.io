---
title: Requirements
layout: page
permalink: /requirements/
---

## Linux

Kereru should work with most 64-bit Linux systems.

Kereru has been tested with Ubuntu 20.10 x64, Debian 10 x64, Fedora 33, CentOS 8.3, Arch Linux, and FreeBSD 12.2 x64.

Packaged versions and source binaries are listed in the [Downloads]({% link pages/downloads.md %}).

## Database

Kereru requires [MySQL](https://www.mysql.com/) or [MariaDB](https://mariadb.org/) to be installed and running.

The application will generate the database schema for an existing database and database user on first run.

The database and database user must be created manually before use.

Step by step instructions are available for [Database Setup]({% link pages/database.md %}) in the Documentation.

## Video (Optional)

Kereru requires [FFmpeg](https://ffmpeg.org/) to be installed for video support.

## Email (Optional)

Kereru requires a Simple Mail Transfer Protocol (SMTP) server on <tt>localhost:25</tt> to send self-service password reset emails.

