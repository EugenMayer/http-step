# Rundeck HTTP Workflow Step Plugin
This plugin provides a way to send HTTP requests as part of
a [Rundeck](http://rundeck.org) workflow step. It is somewhat
based on https://github.com/rvs-fluid-it/rundeck-httppost-plugin.

[![Build Status](https://travis-ci.org/ikogan/rundeck-http-plugin.svg?branch=master)](https://travis-ci.org/ikogan/rundeck-http-plugin) [![Dependency Status](https://www.versioneye.com/user/projects/561e86d336d0ab00160001a9/badge.svg?style=flat)](https://www.versioneye.com/user/projects/561e86d336d0ab00160001a9)

## Features

- GET, POST, PUT, PATCH, DELETE, HEAD, OPTIONS
- Authentication: BASIC or OAuth 2.0
- Project or Framework level configuration

## Caveats

OAuth 2.0 only supports the Client Credentials Grant Type. The OAuth
configuration is per-project or per-framework. This means that each job
will share the entire project or entire frameworks credentials. However,
this allows those credentials to be externalized into the framework
configuration and avoids them being exported with projects.

## Todo

- Support request parameters from config and/or data
- Support request body from config and/or data
- Find a way to support per-job authentication settings?
