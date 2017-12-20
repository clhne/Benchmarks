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

Linear regression, as in `mp-test/tf.py` using NGC Docker Tensorflow image `17.12`:

- `steps=30000, nin=8192, nout=512, nbatch=64`

  - Titan V : 55 seconds
  - GTX 980ti: 67 seconds
  
- `steps=1000, nin=8192, nout=8192, nbatch=64`:

  - Titan V: 9 seconds
  - GTX 980ti: 19 seconds

- `steps=1000, nin=8192, nout=8192, nbatch=512`:

  - Titan V: 14 seconds
  - GTX 980ti: 42 seconds
  
- `steps=1000, nin=8191, nout=8191, nbatch=511` (**not** mutliples of `8`):

  - Titan V: 25 seconds
  - GTX 980ti: 43 seconds
