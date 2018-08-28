---
layout: page
title: BFM Quick Guide
id: quick-guide
description: |
---

## Installation Requirements

<br/>

#### Supported architectures:

- Linux
- Mac OSX (Darwin)
- IBM iDataplex dx360

#### Software requirements:

- PERL (version 5.8.2 and above), including Switch module.
- FORTRAN 90/95 compiler. Under linux and Mac OSX the model can be currently compiled with gfortran (version 4.6 or higher) and ifort.
- [NetCDF library](http://www.unidata.ucar.edu/software/netcdf). It is mandatory that the library has been compiled with the same compiler used for the model compilation (as F90 netcdf module is used).
- [GNU make](https://www.gnu.org/software/make/). Makefile only works with GNU make, therefore substitute your system make or use an alias to ensure that the right one is set in case you are not on a linux machine.

<br/>

### Get started with STANDALONE preset

<br/>

Configuration and deployment of the model is done automatically by the script bfm_configure.sh found in the build directory. The minimal user local settings for compilation is provided by means of the environmental shell variable BFMDIR

```bash
export BFMDIR=/path/to/bfm
cd $BFMDIR/build
./bfm_configure.sh -h
```

The user-dependent options are set either through the command line of the script or by adjusting (or adding) an architecture file in directory $BFMDIR/compilers. Default file is gfortran.inc. The standard GNU gmake variables are used for compiler and archiver names. Remember to add the right path for the NetCDF library files in the appropriate .inc file.

If preset is not specified (see below),  the STANDALONE_PELAGIC configuration is compiled by default with the command

```bash
./bfm_configure.sh -gcd
```

(see the script help for details on the options) and if successful will produce the following output

```bash
.................................. Makefile is ready.
STANDALONE_PELAGIC generation done!
Starting STANDALONE_PELAGIC compilation...
STANDALONE_PELAGIC compilation done!
Go to $BFMDIR/run/standalone.pelagic and execute command:
./bfm_standalone.x
```

The execution of the configuration script creates the executable and the running environment for the default preset of the STANDALONE model (called STANDALONE_PELAGIC). The list of the available presets is obtained with the command

```bash
./bfm_configure.sh -P 
```

The generated namelists are copied to the directory $BFMDIR/run/standalone.pelagic and the model is run by executing

```bash
./bfm_standalone.x
(./bfm_standalone.x &> outputfile to redirect the output messages to a file in bash.)
```

The following test cases are available:

Simple carbonate equilibrium test (STANDALONE_CO2TEST)

```bash
./bfm_configure.sh -gcd -p STANDALONE_CO2TEST
```

Surface layer model in a temperate pelagic water column with seasonal sinusoidal variability (STANDALONE_PELAGIC)

```bash
./bfm_configure.sh -gcd -p STANDALONE_PELAGIC
```

---

All details about model description, installation, compilation and model code structure are available in BFM Core Manual (see Documentation section).


