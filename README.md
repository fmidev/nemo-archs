# nemo-archs

Configuration files for an Archipelago Sea / Åland Sea setup for the NEMO ocean model.

## Background

This setup has 0.25 NM (nautical mile) or approximately 500 m horizontal resolution.

The version in this repository is a development version of the configuration that uses NEMO 4.
There are bound to be bugs and suboptimal settings. Any settings may change without prior warning.

## Getting started

The EXP00 directory has all published files for a small test run of the configuration.
The test run uses ERA5 atmospheric forcing and Copernicus CMEMS boundary condition.
To run, you'll need to compile NEMO 4 with seaice and NetCDF 4. You can use the SPITZ12
setup as a starting point.

Your makenemo line may look something like:
```
./makenemo -r SPITZ12 -n NEMOARCHS -m yourarch add_key key_netcdf4
```

and cpp file:
```
 bld::tool::fppkeys key_mpp_mpi key_iomput key_si3 key_netcdf4
```

The NEMO version that has been tested is version 4.0.3. There are no source code changes. Please note
that you need to add a bathymetry file to this configuration, which you can compile from public sources,
e.g. from BSBD.

## Authors and acknowledgements

This configuration has been developed at the Finnish Meteorological Institute (FMI) by
Antti Westerlund. Elina Miettunen from the Finnish Environment Institute (Syke) contributed to the 
development work significantly. Furthermore, a number of other people have contributed, 
see the cited paper for more information.

If you refer to this configuration in your work, please cite at least Westerlund et al. (2021) somewhere in your paper. Optionally, you can also refere to this GitHub repository directly.

This configuration has been used also in the paper Miettunen et al. (2023).


## Contact and contributing

This repository is maintained by Antti Westerlund.

E-mail: antti.westerlund (at) fmi.fi, X: [@AnttiWesterlund](https://twitter.com/AnttiWesterlund).

Contributions and improvements are most welcome. If you wish to use this configuration for your work,
please consider contacting us to discuss possible collaborations.

## Licenses and permissions

The NEMO model is licensed under the CECILL licence, so all files originating from there use that licence.
Any new files and changes specific to this configuration are licenced under the MIT License in addition
to the CECILL licence.

Please see the file LICENCE for more information.

## References

Westerlund, A., Miettunen, E., Tuomi, L., and Alenius, P.: Refined estimates of water transport through the Åland Sea in the Baltic Sea, Ocean Sci., 18, 89–108, [https://doi.org/10.5194/os-18-89-2022], 2022. 

Miettunen, E., Tuomi, L., Westerlund, A., Kanarik, H., and Myrberg, K.: Transport dynamics in a complex coastal archipelago, EGUsphere \[preprint\], [https://doi.org/10.5194/egusphere-2023-1547], 2023. 



