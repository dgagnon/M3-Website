---
title: "Overview"
linkTitle: "Overview"
weight: 1
description: >
  Documentation for M4 System, the Modern Monitoring and Management System.
---

{{% pageinfo %}}
Work in Progress.  Feel free to contribute with a [Pull Request](https://github.com/m4system/m4system.ca/pulls)!
{{% /pageinfo %}}


## Features

* Web-based multi-tenant SLA management system using django and python 3
* Mysql for general storage
* InfluxDB for historical time-series storage
* Grafana for graphing historical data
* Memcached for volatile cache
* RabbitMQ as distributed queuing system
* Djcelery as task runner
* HTML5 responsive frontend with static asset compression
* Per-group views
* Backend admin panel using Jet django-admin
* Asset list
* Assign checks to multiple assets
* SNMP and bash exec available (numbers, strings, booleans)
* Assign warning and critical thresholds to checks
* Assign SLAs to checks
* Checks, thresholds and SLAs can be configured to fail on 1 or all hosts/checks assigned for complex scenarios like redundant pumps.
* Email template editor in the Back-end
* Group-based notifications.
* Users can edit their own notification email in the frontend.
* View check info, last 30 minutes and download historicals from the front end as a user.
* Group-based Permission system for silencing checks, seeing info, graph and historical
* Metadata system
* Reports using django management commands
* Full audit log of object modifications (django-reversion). events, errors.
* Temporary silence checks from the front-end
* SNMP Traps collection (for vertiv gear)
* Easily identify threshold and SLA faults on the front-end with color transitions

## Why do I want it?

With M4 System, you can address complex scenarios involving many hundreds of devices.  
Manage everything from a web UI with access control and a full audit trail.

* **What is it good for?**: SNMP monitoring.

* **What is it not good for?**: Network and System Monitoring.  While it is able to do such monitoring, other software will do a better job.

* **What is it *not yet* good for?**: Modbus Monitoring.

## Where should I go next?

Interested ? Keep on reading.

* [Getting Started]({{< relref "docs/tutorials/_index.md" >}}): Get started with M4 System
* [Screenshots]({{< relref "docs/screenshots/_index.md" >}}): Check out some screenshots!

