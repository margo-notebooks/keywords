# KWP 1: `ignore-cell`

```yaml:meta
KWP: 1
keyword: ignore-cell
statement type: directive
purpse: ignore a cell in non-notebook contexts
author: Jake Kara <jake@jakekara.com>
status: Accepted
created: March 1, 2021
```

## Abstract

To use notebooks as modules, it is necessary to prevent cells from being included in non-notebook contexts, such as during importation.

## Motivation

In order to develop [Margo Loader](https://github.com/margo-notebooks/margo-loader-py), it became clear that there was a need to ignore cells that made sense in a notebook context but not in a module context.  

Jupyter Notebooks are written differently from other Python source code files. They may include code that is reusable alongside code which is not reusable. For example, imagine a notebook that in one cell defines a function to extracts five dominant colors from an image, and then in a subsequent cell demonstrates the use of that function on a specific input image. The second cell should not be exported because it doesn't do add anything useful to the client view of the notebook. However, we would not want a notebook author to exclude such a demonstration in their notebook in order to make it a useful module. So, the `ignore-cell` directive is intended to mark cells such as that one for exclusion in non-notebook contexts.

## Use cases

This directive is intended to be used when using a Notebook document in a non-notebook execution environment, such as when the notebook is being used a module. It may also be useful in other contexts, such as when executing a notebook as a script or workflow task.

It is up to application developers to determine if their context should exclude
cells marked with the `ignore-cell` directive.

## Usage

`ignore-cell` is a directive-type Margo statement, not an assignment. It is intended to be used in the preamble of a cell:

```python
# :: ignore-cell ::

print("The contents of this cell will be skipped during import")
```
s