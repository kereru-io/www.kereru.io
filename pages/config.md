---
title: Config File
layout: page
permalink: /config/
---

## Location

The config file by default is at <tt>/etc/kereru/config.yml</tt>

## Generating the Config File

From a root shell, run the Kereru first time setup tool:

```console
# kereru_setup
```

The tool will ask a series of questions for Kereru configuration and write the config file.

Default options are suggested for most settings which should get you a working config file.

## Config Options

### Database Options

| key | meaning | default |
| -- | -- | -- |
| **DatabaseName** | Name of the database instance | <tt>kereru</tt> |
| **DatabaseUser** | Name of the database user | <tt>twitter</tt> |
| **DatabasePassword** | Password for the database user | |
{: .table}

### Web server Options

| key | meaning | default |
| -- | -- | -- |
| **WebPort** | What port number will the application run on | <tt>8080</tt> |
| **PathToWebRoot** | Absolute path for the web templates | <tt>/usr/share/kereru</tt> |
{: .table}

### Email Options

| key | meaning | default |
| -- | -- | -- |
| **WebHost** | Host name of the web server, used for password reset emails | <tt>localhost</tt> |
{: .table}

### Security Options

| key | meaning | default |
| -- | -- | -- |
| **TLS** | Controls if the application is running with TLS | <tt>false</tt> |
| **PathToCert** | Absolute file path to the TLS Certificate, only relevant if **ServerTLS** is set to True | |
| **PathToKey** | Absolute file path to the TLS Private key, only relevant if **ServerTLS** is set to True | |
| **CsrfToken** | A security token unique to each instance of Kereru | set to random unique value by <tt>kereru_setup</tt> |
| **SecureCookie** | Should the application mark cookies as secure | <tt>false</tt> |
{: .table}

### Image and Video Upload Options

| key | meaning | default |
| -- | -- | -- |
| **UploadPath** | Absolute path to the uploads directory for images and video | <tt>/var/kereru/uploads</tt> |
{: .table}

### Twitter API Options

| key | meaning | default |
| -- | -- | -- |
| **OauthConsumerKey** | Twitter OAuth 1.0a API Consumer Key | |
| **OauthConsumerSecret** | Twitter OAuth 1.0a API Consumer Secret | |
| **OauthToken** | Twitter OAuth 1.0a Token | |
| **OauthTokenSecret** | Twitter OAuth 1.0a Token Secret | |
{: .table}

## Development

| key | meaning | default |
| -- | -- | -- |
| **DebugLevel** | Level of debug output | 1 |
{: .table}

## Multiple Instances

| **Delay** | Delay in seconds to wait after scheduled time before sending tweets | 0 |
{: .table}

