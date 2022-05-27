# Dashboards
**PowerBI** Containers for data automation, using [**PLP-IIoT**](https://github.com/PLP-Data-automation/IIoT-PLP) _Python-package_.
Installation required, refer to **PLP-IIoT** module.

## Usage Example

The following **PowerBI** container use Python-scripts, available at [test](https://github.com/PLP-Data-automation/IIoT-PLP/tree/main/test).

On a new **PowerBI** dashboard, select _get data_, _more_ options and find _python_ data source option. Copy any of the **power_bi_run.py** scripts on the panel. For example:

``` sh
from DataAccess.Query import run_query

if __name__ == "__main__":
  try:
      results = run_query()
      df = results["reduced-filter"]
      print( df )
  except UnboundLocalError:
      print( "Loading failed!" )
```

This script will load in **Power BI** a reduced and filtered version of the **DataAccess** table results.

## License
MIT

[//]: # (Author: Fuentes Juvera, Luis [LuidDFJ]: <https://github.com/LuisDFJ> )