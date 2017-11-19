# Benchmarks

2.1k-parameters RNN, 10 epochs:

- Threadripper 1900x (8 cores, 16 HT, 3.8GHz, NUMA mode), CPU only: 67 minutes
- Threadripper 1900x (8 cores, 8 HT, 3.8GHz, NUMA mode), CPU only: 59 minutes
- Threadripper 1900x, GTX 980ti using 16 PCIe3.0 lanes: 4 minutes
- i7-2760QM (4 cores, 4HT, 2.4GHz, no TurboBoost), CPU only: 111 minutes
- i7-2760QM, GTX 980ti using 1 PCIe2.0 lane: 10 minutes
