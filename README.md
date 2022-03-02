# data_aggregator

A Python solution using a combination of array vectorization, JIT compilation and C-arrays to improve performance. 


## Files
Detailed notes are given in the individual files.

### File 1: data_aggregator_logic_tests.ipynb
Here we test out the logic on simulated data points, and benchmark the performance of the algorithm.

[Link to file 1](https://github.com/dineshpinto/data_aggregator/blob/main/data_aggregator_logic_tests.ipynb)


### File 2: data_aggregator_main.ipynb
Here the logic is used by executing the binary file and analyzing its input.

[Link to file 2](https://github.com/dineshpinto/data_aggregator/blob/main/data_aggregator_main.ipynb)

## Further improvements
- Compile Numba against the Intel SVML libraries for further performance enhancement (currently not possible on M1 arch)
- Added parallel processing in Numba for processing distinct arrays concurrently (should be relatively trivial, but may require dropping down to `ctypes` arrays to ensure processes can write concurrently)
