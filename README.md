# Simulation Headers for HLS Designs
This repo includes headers required for simulating designs targeted at Vivado HLS, in the absence of a Vivado/Vitis installation. It is not a complete solution, for example:
* there is no stream implementation (yet) - use in conjunction with [hlslib](https://github.com/definelicht/hlslib) to get stream functionality in simulation.
* no support for `qdma_*` types
* and too many others to list

Vitis HLS supports the `half` reduced-precision floating point datatype which is not part of C++ but is provided in this repo through `half.hpp` which needs to be included explicitly in your code.

# Acknowledgements
The headers in this project were collected from:

* Half-precision support ported from the [ROCm half-precision repo](https://github.com/ROCmSoftwarePlatform/half) which itself is a fork of [the half library](http://half.sourceforge.net) 
* arbitrary precision implementations added from [Xilinx HLS AP types repo](https://github.com/Xilinx/HLS_arbitrary_Precision_Types)
* `ap_axi*` types from the [Xilinx Merlin Compiler repo](https://github.com/Xilinx/merlin-compiler)
