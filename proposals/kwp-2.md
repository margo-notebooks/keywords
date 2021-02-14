
```yaml:meta
KWP: 1
keyword: submodule
statement type: assignment
purpose: group cells into virtual submodules
author: Jake Kara <jake@jakekara.com>
status: Accepted
created: March 1, 2021
```

## Abstract

When importing notebooks as modules, indicate that a cell should be executed inside a virtual submodule of the notebook.

## Motivation

## Use cases

## Usage

```python
# :: submodule: "grumpy"
```

```python
# :: submodule: "nice"
```