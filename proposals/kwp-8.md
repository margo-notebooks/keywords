# KWP 8: `stop-module` and `start-module`

```yaml:meta
KWP: 8
keyword: `stop-module` and `start-module`
statement type: directive
purpose: ignore cell and subsequent cells in non-notebook contexts
author: Jake Kara <jake@jakekara.com>
status: Accepted
created: June 2, 2021
```

## Abstract

Building upon `ignore-cell` [(KWP-1)](./kwp-1.md), it is often useful to ignore
multiple sequential cells without having to annotate each cell with the
`ignore-cell` directive.

## Motivation

In order to load Jupyter Notebooks as Python modules,
[Margo Loader](https://github.com/margo-notebooks/margo-loader-py), introduced a
strategy of ignoring cells during import with `ignore-cell`. In order to ignore
multiple, sequential cells at once, `stop-module` and `start-module` are
introduced.

## Use cases

Ignoring cells while importing a Jupyter Notebook as a Python module.

## Usage

```python:margo
# :: stop-module

print("This cell will be ignored")
```

```python:margo
# :: stop-module

print("This cell will also be ignored")
```

```python:margo
# :: start-module
# This cell will not be ignored

def say_goodbye():
    return "Goodbye!"
```
