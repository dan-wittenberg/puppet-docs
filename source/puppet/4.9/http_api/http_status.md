---
layout: default
built_from_commit: 629a508e98d21e5fe98a8a35b2c31dbc62e6a669
title: 'Puppet HTTP API: Status'
---

Status
=============

The `status` endpoint provides information about a running master.

Find
----

Get status for a master

    GET /puppet/v3/status/:name?environment=:environment

The `environment` parameter and the `:name` are both required, but have no
effect on the response. The `environment` must be a valid environment.

### Supported HTTP Methods

GET

### Supported Response Formats

PSON

### Parameters

None

### Example Response

    GET /puppet/v3/status/whatever?environment=env

    HTTP 200 OK
    Content-Type: text/pson

    {"is_alive":true,"version":"3.3.2"}

Schema
------

A status response body conforms to [the status schema.](../schemas/status.json)
