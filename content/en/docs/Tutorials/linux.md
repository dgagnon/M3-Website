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

```
apt-get install python3.5-dev libmemcached-dev
wget https://bootstrap.pypa.io/get-pip.py
python3.5 get-pip.py
```

## Install requirements

```
pip3.5 install -r requirements.txt
```
