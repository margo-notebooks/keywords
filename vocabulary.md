# Margo Vocabulary 0.0.1

## Accepted  

### ignore-cell

Notes that a cell should be excluded from the notebook when the notebook is being imported as a module. [KWP-1](proposals/kwp-1.md)

### submodule

Notes that a cell should be included in a virtual submodule with the notebook is being imported as a module. [KWP-2](proposals/kwp-2.md)

### requirements.txt

Lists the Notebook's dependencies in the same format as a Python ]][requirements.txt](https://pip.pypa.io/en/stable/reference/pip_install/#requirements-file-format). [KWP-3](proposals/kwp-3.md)

### interface.inputs

Lists local files that are required prior to executing a notebook as a standalone script. [KWP-4](proposals/kwp-4.md)  

### interface.outputs

Lists local files that are created by executing a notebook as a standalone script. [KWP-5](proposals/kwp-5.md)

### cell-id

Notes a unique identifier for a cell. [KWP-6](proposals/kwp-6.md)  

### rel.[relationship]

Notes a relationship from the current cell to the specified target cell. [KWP-7](proposals/kwp-7.md)