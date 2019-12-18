---
title: "Linux Setup"
date: 2017-01-05
weight: 4
description: >
  Raspbian Setup
---

{{% pageinfo %}}
Work in Progress.  Feel free to contribute with a [Pull Request](https://github.com/m4system/m4system.ca/pulls)!
{{% /pageinfo %}}

## Install python 3.5
apt-get install python3.5-dev
wget https://bootstrap.pypa.io/get-pip.py
python3.5 get-pip.py

## Install Dependancies
apt-get install libmemcached-dev libsnmp-dev libmariadb3

## Install requirements
pip3.5 install -r requirements.txt

## Fix mariadb librairy paths
ln -s /usr/lib/arm-linux-gnueabihf/libmariadb.so.3 /usr/lib/arm-linux-gnueabihf/libmariadbclient.so.18


```
This is the final element on the page and there should be no margin below this.
```
