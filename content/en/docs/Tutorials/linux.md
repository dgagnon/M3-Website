---
title: "Linux Setup"
date: 2017-01-05
weight: 4
description: >
  Tested on Raspbian.
---

{{% pageinfo %}}
Work in Progress.  Feel free to contribute with a [Pull Request](https://github.com/m4system/m4system.ca/pulls)!
{{% /pageinfo %}}

## Install python 3.5 and other dependancies

```
# python
apt-get install python3.5-dev libmemcached-dev rabbitmq-server 
wget https://bootstrap.pypa.io/get-pip.py
python3.5 get-pip.py
# Node
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
nvm install node
npm install lessc -g
# rabbit auth
rabbitmqctl add_user m4 changeme
rabbitmqctl add_vhost m4
rabbitmqctl set_user_tags m4 m4
rabbitmqctl set_permissions -p m4 m4 ".*" ".*" ".*"
```


## Setup SNMP

Allow localhost with community "public". 

This will allow M4 to poll your local SNMP deamon to get some fresh data.

Edit the HostCheck and enter an OID which outputs a number (see snmpwalk). 

## Setup M4

```
pip3.5 install -r requirements.txt
pip3.5 install -e .
manage migrate djangoplugins
manage migrate
python3.5 manage.py loaddata fixtures/auth.json
python3.5 manage.py loaddata fixtures/user.json
python3.5 manage.py loaddata fixtures/djcelery.json
python3.5 manage.py loaddata fixtures/scheduler.json
python3.5 manage.py loaddata fixtures/webview.json
manage collectstatic
```

## Run M4

```
start.sh
```

## Login to M4

http://127.0.0.1:8000

m4 / Changeme1!