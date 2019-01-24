# Window matconvnet settings

**Environment**

---

- Window10
- VS2013
- MATLAB2018b
- CUDA9.0
- CUDNN7.4.2
- Matconvnet

---

- download matconvnet [[link](http://www.vlfeat.org/matconvnet/)]
- download cuda9.0 [[link](https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exenetwork)]
  - ex: cuda_9.0.176_win10_network
  - default settings
- download cudnn7.4.2 for CUDA 9.0 [[link](https://developer.nvidia.com/rdp/cudnn-download)]
  - install guideline [[link](https://docs.nvidia.com/deeplearning/sdk/cudnn-install/index.html)]
  - cuDNN Library for Windows 10 (ex: cudnn-9.0-windows10-x64-v7.4.2.24)
  - unzip file
  - Copy the following files into the CUDA Toolkit directory.
    - `Copy <installpath>\cuda\bin\cudnn64_7.dll to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\bin.`
    - `Copy <installpath>\cuda\ include\cudnn.h to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\include.`
    - `Copy <installpath>\cuda\lib\x64\cudnn.lib to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\lib\x64.`
  - Click Environment Variables at the bottom of the window.
    - Ensure the following values are set:
    - `Variable Name: CUDA_PATH`
    - `Variable Value: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0`
- Install and compiling the library [[link](http://www.vlfeat.org/matconvnet/install/)]
  - open MATLAB and go to matconvnet folder
  - `mex -setup (set VS2013)`
  - `addpath(genpath('.'))`
  - `vl_compilenn('gpu', true)`

