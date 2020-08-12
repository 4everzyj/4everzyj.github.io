---
title: ubuntu disk io problem
date: 2020-08-12 18:56:11
categories:
- tools
tags:
- tools
- ubuntu
- bug
---

## Performance

- Slow reading and writing disk

## Enviroment

- ubuntu 16.04 LTS

## Command

### 1. iostat

``` bash
$ iostat
```

if iostat not installed
``` bash
$ sudo apt install sysstat
```

you can add some parameter like:
``` bash
$ iostat -x 1
```

### 2. iotop

you can use `iotop` to watch each process
```bash
$ sudo iotop
```

if iostat not installed
``` bash
$ sudo apt install iotop
```

you can add some parameter like:
``` bash
$ sudo iotop -P
$ sudo iotop -oP
```
