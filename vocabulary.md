# Margo Vocabulary 0.0.1

## Accepted  

### kwp-1: `ignore-cell`

Notes that a cell should be excluded from the notebook when the notebook is being imported as a module. [Read the full proposal](proposals/kwp-1.md).

### kwp-2: `submodule`

Notes that a cell should be included in a virtual submodule with the notebook is being imported as a module.  

[Read the full proposal](proposals/kwp-2.md).

### kwp-3: `requirements.txt`

Lists the Notebook's dependencies in the same format as a Python [requirements.txt](https://pip.pypa.io/en/stable/reference/pip_install/#requirements-file-format) file. [Read the full proposal](proposals/kwp-3.md).

### kwp-4: `interface.inputs`

Lists local files that are required prior to executing a notebook as a standalone script. 

### kwp-5: `interface.outputs`

Lists local files that are created by executing a notebook as a standalone script.  

### kwp-6: `cell-id`

Notes a unique identifier for a cell.  

### kwp-7: `rel.[relationship]`

Notes a relationship from the current cell to the specified target cell.

### kwp-8: `stop-module` and `start-module`

Notes the current cell and all subsequent cells should be excluded (in the case
of `stop-module`) or included (`start-module`) when the notebook is being imported as a cell. [Read the full proposal](proposals/kwp-8.md).  
