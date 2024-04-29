# DestinE_EnSys_Demonstrator
Demonstrator of the [Destination Earth Use Case Energy Systems](https://stories.ecmwf.int/energy-systems/)

## Features
The DestinE Energy Systems Demonstrator is a simplified adaptation of the [European Resources Adequacy Assessment](https://www.entsoe.eu/outlooks/eraa/) (ERAA), using only publicly available data and two different open-source energy system modelling frameworks ([REMix](https://github.com/dlr-ve-esy/remix-eraa) and [PyPSA](https://github.com/dlr-ve-esy/pypsa-eraa)). It includes submodules for

a) data collection and preprocessing ([resources submodule](https://github.com/dlr-ve-esy/eraa-resources))

b) model building and solving in either of the two energy system modelling frameworks.

All parts are implemented in respective automated [Snakemake](https://snakemake.readthedocs.io/en/stable/) workflows.

In particular, the Demonstrator derives leas-cost operation strategies for a simplified European power system. This includes the operation of generation and storage capacities with perfect foresight over full years in hourly resolution and the transport of electricity between the European bidding zones for electricity (or the European countries, respectively) along simplified transmission links with net transfer capacities. All data needed to build this model is obtained from websites of the European Network for Transmission System Operators for Electricity (ENTSO-E). The data collection module is implemented and tested for ERAA version 2022 and 2023 and includes public versions of the *Pan-European Market Modeling Database* (PEMMDB) and the *Pan-European Climatic Database* (PECD). Depending on the ERAA version, 35 weather years and up to 5 target years (scenarios for capacity expansion) can be simulated.

Finally, different adequacy indicators can be derived from the power system simulations, including the *Loss of Load Expectation* (LOLE) and the *Energy not served* (ENS).

The release of additional features on asesssing the sensitivity of the adequacy assessment on the choice of the meteorological data set or on reducing the complexity of the workflows is under preparation.

## Contributing
We invite everyone to use and test this software. If you encounter problems or have ideas for improvements please open an issue or a merge request. Any contribution is highly appreciated.

To clarify the intellectual property license granted with contributions from any person or entity to this repository, Deutsches Zentrum für Luft- und Raumfahrt e. V. (German Aerospace Center, "DLR") must have a [Contributor License Agreement](ContributorLicenseAgreement.md) on file that has been signed by each Contributor. This is for your protection as a contributor as well as the protection of DLR. It does not change your rights to use your own contributions for any other purpose.

## Code of Conduct
Please respect our [Code of Conduct](CODE_OF_CONDUCT.md)

## License
Copyright 2023-2024 (c) DLR, all rights reserved

This repository is maintained by the [German Aerospace Center](https://dlr.de/ve/en) (DLR) in support of ECMWF's role in [Destination Earth](https://destination-earth.eu) funded by the European Union and published under the open-source [MIT License](LICENSE).
