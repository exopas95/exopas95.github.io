---
layout: post
title:  "Working with Dates and Times in Python"
date:   2020-06-13T10:06:52-05:00
author: TreeNulbo
categories: Intermediate-Python
---

이번 포스트에서는 파이썬을 사용하여 시간을 다루는 방법에 대해서 설명해보고자 한다. 데이터 전처리에서 시간 데이터를 다루는 일은 매우 많으며 그 방법 또한 매우 다양하다. 여기서는 여러가지 모듈 중에서도 **datetime** 모듈을 사용하여 시간 데이터를 다뤄보고자 한다.

## 데이터 불러오기
먼저 이번 포스트에서 사용할 데이터 셋을 불러오자. 데이터 셋은 **Obama White House Archives Site**에서 가져온 2015년 워싱턴 방문 기록을 사용할 것이다.
```python
from csv import reader
open_file = open("potus_visitors_2015.csv")
read_file = reader(open_file)
potus = list(read_file)
potus = potus[1:]
```

## datetime 모듈
**datetime** 모듈을 사용하기에 앞서 간단한 예시를 들어보자. 
```python
import datetime as dt

ibm_founded = dt.datetime(1911, 6, 16)
man_on_moon = dt.datetime(1969, 7, 20, 20, 17)
print(ibm_founded)
print(man_on_moon)
```
```python
1911-06-16 00:00:00
1969-07-20 20:17:00
```

## datetime format
```python
date_format = "%m/%d/%y %H:%M"

for row in potus:
    start_date = row[2]
    start_date = dt.datetime.strptime(start_date, date_format)
    row[2] = start_date
```