Convenient (hopefully) pre-built binaries of popular Mochimo software.

## Latest Downloads
Head to [Releases](https://github.com/chrisdigity/mochimo-binaries/releases) for binary package downloads.

## Selecting a GPU Miner package
First check the NVIDIA Driver on the machine:
```
miner@mcmrig:~# nvidia-smi
Mon Oct 17 14:42:59 2022
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 515.76.02    Driver Version: 517.48       CUDA Version: 11.7     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA GeForce ...  On   | 00000000:01:00.0  On |                  N/A |
| 57%   50C    P0   119W / 350W |   1901MiB / 12288MiB |      1%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+
```
... Driver Version: **517.48**

Packages are labelled with minimum compatible versions, in the format:
```
mcmminer-<MCM_version>.<OS>.cuda-<CUDA_version>-<NVIDIA_version>.<zip>
```
... so for the above machine, we can use any of the packages with **NVIDIA_version <= 517.48**.

## Miner Usage
Illamanudi Mining Pool:
- `pool_ip` Pool Proxy Client IPv4 address
- `pool_port` 2195 (Default)
```
./mcmminer --pool <pool_ip> --port <pool_port>
```

## Addtitional resources
- [Mochimo Repository](https://github.com/mochimodev/mochimo)
- [CUDA Toolkit Downloads](https://developer.nvidia.com/cuda-downloads)
- [CUDA Toolkit and Corresponding Driver Versions](https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html#cuda-major-component-versions__table-cuda-toolkit-driver-versionshttps://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html)
