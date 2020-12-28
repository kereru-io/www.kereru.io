---
title: Quick Start
layout: page
permalink: /quickstart/
---

## Installation

1. Install and run [Requirements]({% link pages/requirements.md %})
1. Configure the [Database]({% link pages/database.md  %})
1. [Download]({% link pages/downloads.md %}) and install Kereru for your system
1. Generate [Twitter API Keys]({% link pages/api.md %})

## Configuration

From a root shell, run the Kereru first time setup tool

```console
# kereru_setup
```

Answer the questions, defaults for most settings should get you a working system.

## Launch Kereru web application

The [Config File]({% link pages/config.md  %}) must exist before running the Kereru web application

Packaged versions create a <tt>kereru</tt> user and group.

To run the Kereru web application using systemd:

```console
# systemctl enable --now kereru_app.service
```

To run the Kereru web application manually, launch as the <tt>kereru</tt> user:

```console
$ kereru_app
```

## Launch Kereru bot

The [Config File]({% link pages/config.md  %}) must exist before running the Kereru bot

The Kereru bot is a seperate service that sends tweets. The Kereru bot *must* be running for tweets to send.

To run the Kereru bot using systemd:

```console
# systemctl enable --now kereru_bot.service
```

To run the Kereru bot manually, launch as the <tt>kereru</tt> user:

```console
$ kereru_bot
```

## First Run

Connect to the Kereru web application, by default <tt>http://localhost:8080/<tt>.

The Kereru web application will prompt to create the first account. This account will be the Kereru adminstrator.

## Your First Tweet

In the Kereru web application, create a new tweet from the "New Tweet" page from the navigation menu.

A tweet requires a date and time in Coordinated Universal Time (UTC) and a message. Saving a new tweet will create a Draft status tweet.

To change a tweet's status, click the status from the Status column on the "List Tweets" page. A Draft status tweet is first moved to Reviewed status, then to Ready status.

Tweets that are Ready status will be sent after the tweet's date and time has been reached.
