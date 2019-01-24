# Window10-VS2013-MATLAB2018b-Matconvnet
Window10+VS2013+MATLAB2018b+Matconvnet

- download matconvnet [[link](http://www.vlfeat.org/matconvnet/)]
- download cuda [[link](https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exenetwork)]
  - ex: cuda_10.0.130_win10_network
  - default settings
- download cudnn [[link](https://developer.nvidia.com/rdp/cudnn-download)]
  - cuDNN Library for Windows 10 (ex: cudnn-10.0-windows10-x64-v7.4.2.24)
  - unzip file
  - Copy the following files into the CUDA Toolkit directory.
    - `Copy <installpath>\cuda\bin\cudnn64_7.dll to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\bin.`
    - `Copy <installpath>\cuda\ include\cudnn.h to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\include.`
    - `Copy <installpath>\cuda\lib\x64\cudnn.lib to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0\lib\x64.`
  - Click Environment Variables at the bottom of the window.
    - Ensure the following values are set:
    - `Variable Name: CUDA_PATH`
    - `Variable Value: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0`
- Install and conpiling the library [[link](http://www.vlfeat.org/matconvnet/install/)]
  - open MATLAB and go to matconvnet folder
  - mex -setup (set VS2013)
  - vl_testnn('gpu', true)

