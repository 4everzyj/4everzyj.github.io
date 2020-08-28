---
title: debug python memory leak
date: 2020-08-28 17:21:02
categories:
- tools
tags:
- tools
- python
---

## Aim

- find where the memory leak happened

## Enviroment

- python3.6

## Install

```bash
$ pip3 install pympler
```

## Code

### 1. print_diff step by step

``` python
from pympler import tracker


tr = tracker.SummaryTracker()

# compare with last summary
tr.print_diff()

```

### 2. print memory useage of each type

```python
from pympler import tracker,summary,muppy


all_objects = muppy.get_objects()
sum1 = summary.summarize(all_objects)
summary.print_(sum1)

```
