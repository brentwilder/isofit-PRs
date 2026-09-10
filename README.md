# ISOSNOW - ISOFIT Snow Surface Model


## Overview

- This diverges from ISOFIT dev branch on around 31 July 2026

- Plan to bring in major updates from future ISOFIT PRs as needed (shown in change log)


## Usage

- See `./isosnow_scripts/`

- The low-rank model files for PV, NPV, and Soil are in the `isosnow_data` folder and must be copied over into the home `~/.isofit/data` directory prior to running.

## Change log

- 10 September 2026: Integrated analytical Jacobian to account for cos_i, instead of relying on numerical, 2-point method (EMIT speed test: 11.22 spectra/sec to 20.99 spectra/sec)

- 9 September 2026: ISOFIT PR-1026, inversion windows patch (EMIT)

- 2 September 2026: ISOFIT PR-1012, MODTRAN TP7 codes

- 2 September 2026: ISOFIT PR-1022, Background topo updates

- 2 September 2026: ISOFIT PR-979, enables setting priors in the surface JSON


## Other (maybe) helpful notes

- Currently `S_hat` does not use any information from `Sa` because we use typically use uninformative priors in the snow model

- `COS_I` is always set to be solved (instead of "flat" or "dem"), and is fully hooked up between surface and atmosphere RT.

