# data_aggregator

A Python solution to the [Messari challenge](https://resonant-zipper-d74.notion.site/Messari-Market-Data-Coding-Challenge-rev-28-Feb-2022-e513357eaeb34b9a9ab9805af37d96b0) using a combination of array vectorization, JIT compilation and C-arrays to improve performance. 


## Files
Detailed notes are given in the individual files.

### File 1: data_aggregator_logic_tests.ipynb
Here we test out the logic on simulated data points, and benchmark the performance of the algorithm.

[Link to file 1](https://github.com/dineshpinto/data_aggregator/blob/main/data_aggregator_logic_tests.ipynb)


### File 2: data_aggregator_main.ipynb
Here the logic is used by executing the binary file and analyzing its input in real-time.

[Link to file 2](https://github.com/dineshpinto/data_aggregator/blob/main/data_aggregator_main.ipynb)

## Further improvements
- Compile Numba against the Intel SVML libraries for further performance enhancement (currently not possible on Mac M1 arch)
- Added parallel processing in Numba for processing distinct arrays concurrently (should be relatively trivial, but may require dropping down to `ctypes` arrays to ensure processes can write concurrently)


## Notes
The conda environment contains a lot of additional libraries for visualization, notebooks etc. The logic itself only requires a minimal subset of those libraries (namely `numpy` and `numba`).
