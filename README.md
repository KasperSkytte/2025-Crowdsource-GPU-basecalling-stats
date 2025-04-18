README
================
Rasmus Kirkegaard
10 April, 2025

## Aim

To make it easier to get an overview of the performance you can get for
nanopore basecalling with
[dorado](https://github.com/nanoporetech/dorado) using a specific GPU.

## How to contribute?
 - Simply download and run the `dorado_basecaller.sh` script. It will download dorado, some 5khz pod5 data
  (from [zenodo](https://zenodo.org/records/15180194)), and run dorado. Please ensure that you are only using a single GPU at once.
 - Add your samples/s output to [google
  form](https://forms.gle/Qw1wiL662YrbHPxk6).

## Script usage
```
$ wget https://raw.githubusercontent.com/Kirk3gaard/2025-Crowdsource-GPU-basecalling-stats/refs/heads/main/dorado_basecaller.sh
$ bash dorado_basecaller.sh -h          
Script to benchmark the basecalling speed of your GPU using dorado. Everything will be run from the current folder. Please publish the results to the community as described here https://github.com/Kirk3gaard/2025-Crowdsource-GPU-basecalling-stats.
Version: 1.0
Options:
  -h    Display this help text and exit.
  -v    Print version and exit.

Additional options can be set by exporting environment variables before running the script:
  - DORADO_VERSION: dorado version to download and use. (Default: 0.9.5)
  - DORADO_MODEL: dorado version to download and use. (Default: sup)
  - DORADO_DEVICE: dorado version to download and use. (Default: cuda:0)
```

As the help text says you can adjust a few things by exporting variables before running the script, fx:
```
$ export DORADO_DEVICE="cuda:1"
$ export DORADO_VERSION="0.9.5"
$ bash dorado_basecaller.sh
```

## Data availability

The collected information is available in [this google
sheet](https://docs.google.com/spreadsheets/d/1p_oqalXtyMomcoeh0CE-crBgxsGifBYMvTR7hHBqmEw/edit?usp=sharing)

## Basecalling performance

The red line indicates the capacity needed to basecall 1 PromethION
flowcell (yielding 150 Gbp/72hours) using the SUP model, the blue line 2 flowcells.

![](README_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->
