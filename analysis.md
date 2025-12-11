---
jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.18.1
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

```python
x = 3
y = 4
x ** y
```

Notebooks can become unreproducible if you do not have access to ALL of the required external dependencies.

Always use relative paths when programming reproducible analytical scripts.

```python
from polars import read_csv

# df = read_csv('/home/cameron/seminar/data/datafile.csv') # if the data doese not exist on other computers; then this wont work
df = read_csv('./data/datafile.csv') # this will be reproducible, provided the data can be downloaded
df
```

```python
from matplotlib import pyplot as plt

fig, ax = plt.subplots()

ax.bar(df['vegetables'], df['count'])
```
