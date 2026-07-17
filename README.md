
# Copernicus Helper

This is a CLI Copernicus helper to make the life easier.

## Envs

Instead of the local `~/.cdsapirc` polluting your home folder, one can use environment variables:

- `CDSAPI_URL` to set the `url`
- `CDSAPI_KEY` to set the personal `key`
- `CDSAPI_RC` to set a curstom location for the configuration file

Setting `url` and `key` by env vars overwrite everything.
Setting the config file by env var is the second choice
Looking at `~/.cdsapirc` is the fallback option.

## Usage


```
usage: copernicus_helper [-h] [--variable VARIABLE] [--country COUNTRY]
                         [--dataset {single-levels,land,pressure-levels}]
                         [--experiment {historical,ssp1_2_6,ssp2_4_5,ssp3_7_0,ssp5_8_5}]
                         [--model MODEL] [--monthly] [--folder FOLDER]
                         [--time-range TIME_RANGE]

Helper to download Copernicus data.

options:
  -h, --help            show this help message and exit
  --variable VARIABLE, -v VARIABLE
                        variable name (default: total_precipitation)
  --country COUNTRY, -c COUNTRY
                        Country to restrict (2chars code, default: IT, you can
                        also select a subunit as in ES:Spain)
  --dataset {single-levels,land,pressure-levels}, --ds {single-levels,land,pressure-levels}
                        Dataset: single-levels (default), land, …, for ERA5.
  --experiment {historical,ssp1_2_6,ssp2_4_5,ssp3_7_0,ssp5_8_5}, -x {historical,ssp1_2_6,ssp2_4_5,ssp3_7_0,ssp5_8_5}
                        Download the given expariment from CMIP6.
  --model MODEL, -m MODEL
                        The model used in the CMIP6 projections.
  --monthly             If monthly values should be fetched instead of daily.
  --folder FOLDER, -o FOLDER
                        Output folder. (default: check if /dataNfs is present,
                        else ~/copernicus_data)
  --time-range TIME_RANGE, -y TIME_RANGE
```
