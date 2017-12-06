# Benchmarks

2.1k-parameters RNN, 10 epochs, Tensorflow, SGD:

- Threadripper 1900x (8 cores, 16 HT, 3.8GHz, NUMA mode), CPU only: 67 minutes
- Threadripper 1900x (8 cores, 16 HT, 3.8GHz Core Boost Disabled, NUMA mode), CPU only: 67 minutes
- Threadripper 1900x (8 cores, 8 HT, 3.8GHz, NUMA mode), CPU only: 59 minutes
- Threadripper 1900x, GTX 980ti using 16 PCIe3.0 lanes: 4 minutes (Windows), 3 minutes (Linux)
- i7-2760QM (4 cores, 4HT, 2.4GHz, no TurboBoost), CPU only: 111 minutes
- i7-2760QM, GTX 980ti using 1 PCIe2.0 lane: 10 minutes

1d Linear regression, Edward, VB 1000 iterations:

- Threadripper 1900x, GTX 980ti using 16 PCIe3.0 lanes: 1.5 minutes
- Threadripper 1900x (8 cores, 16 HT, 3.8GHz Core Boost Disabled, NUMA mode), CPU only: 0.15 minutes

Minimal Stan model compilation:

- i7-2760QM (4 cores, 8HT, 2.4GHz, no TurboBoost), g++: 55 seconds
- i7-2760QM (4 cores, 8HT, 2.4GHz, no TurboBoost), clang++: 35 seconds
- Threadripper 1900x (8 cores, 16 HT, 3.8GHz Core Boost Enabled, NUMA mode), clang++4.0: 42 seconds
- Threadripper 1900x (8 cores, 16 HT, 3.8GHz Core Boost Enabled, NUMA mode), g++ 5.4.0: 38 seconds
