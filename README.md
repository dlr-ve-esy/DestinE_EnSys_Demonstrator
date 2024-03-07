# DestinE_EnSys_Demonstrator
Demonstrator of the Destination Earth Use Case Energy Systems

## Features
The DestinE Energy Systems Demonstrator is a simplified adaptation of the [European Resources Adequacy Assessment](https://www.entsoe.eu/outlooks/eraa/) (ERAA), using only publicly available data and two different open-source energy system modelling frameworks ([REMix](https://github.com/dlr-ve-esy/remix-eraa) and [PyPSA](https://github.com/dlr-ve-esy/pypsa-eraa)). It includes submodules for

a) data collection and preprocessing
b) model building and solving

All parts are implemented in respective automated [Snakemake](https://snakemake.readthedocs.io/en/stable/) workflows but can also be executed in-row using the provided [Snakefile](Snakefile) and [config file](main_config.yaml).

In particular, the Demonstrator derives leas-cost operation strategies for a simplified European power system. This includes the operation of generation and storage capacities with perfect foresight over full years in hourly resolution and the transport of electricity between the European bidding zones for electricity (or the European countries, respectively) along simplified transmission links with net transfer capacities. All data needed to build this model is obtained from websites of the European Network for Transmission System Operators for Electricity (ENTSO-E). The data collection module is implemented and tested for ERAA version 2022 and 2023 and includes public versions of the *Pan-European Market Modeling Database* (PEMMDB) and the *Pan-European Climatic Database* (PECD). Depending on the ERAA version, 35 weather years and up to 5 target years (scenarios for capacity expansion) can be simulated.

Finally, different adequacy indicators can be derived from the power system simulations, including the *Loss of Load Expectation* (LOLE) and the *Energy not served* (ENS).

## Getting Started

## Code of Conduct
Please respect our [Code of Conduct](CODE_OF_CONDUCT.md)

## License
Copyright 2023-2024 (c) DLR

This repository is maintained by the [German Aerospace Center](https://dlr.de/ve/en) (DLR) in support of ECMWF's role in [Destination Earth](https://destination-earth.eu) funded by the European Union and published under the open-source [MIT License](LICENSE).
