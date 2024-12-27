# STU-net 
- https://github.com/uni-medical/STU-Net

## Enviroment
-Windows 11

## requirement
- **anaconda** navigator download:(https://www.anaconda.com/download)
- **pycharm community editor**:(https://www.jetbrains.com/pycharm/download/?section=windows)
- **CUDA Toolkit 12.2 DownloadsA**(https://developer.nvidia.com/cuda-12-2-0-download-archive?target_os=Windows&target_arch=x86_64&target_version=11&target_type=exe_local)


## Edit the system enviroment variables
- Variable:CUDA_PATH; Value:C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.6
- Variable:CUDA_PATH_V12_6; Value:C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.6


## anaconda3
- Environment--->create--->python 3.12.8
### dependencies
- activate <your python>
- pip install batchgenerators (the cmd should show (deeplearning) C:\Users\admin>pip install batchgenerators:where (deeplearning is the name of python enviroment)
- pip install torchinfo
- pip install nibabel
- pip install tqdm
- pip install nnunet

## nnunet 1.7.1 modification 
- check the unzipped file named **nnUNet-1.7.1** download from **(https://github.com/uni-medical/STU-Net)**
- 
- check the file: **(C:\Users\admin\anaconda3\envs\**deeplearning**\Lib\site-packages\nnunet)**
- 
- copy file from **(STU-Net-main\nnUNet-1.7.1\nnunet\network_architecture)** to **(C:\Users\admin\anaconda3\envs\deeplearning\Lib\site-packages\nnunet\network_architecture)**
- 
- copy file from **(STU-Net-main\nnUNet-1.7.1\nnunet\training\network_training)** to **(C:\Users\admin\anaconda3\envs\deeplearning\Lib\site-packages\nnunet\training\network_training)**
- 
- copy python file from **(nnunet/run/run_finetuning.py)** to **(C:\Users\admin\anaconda3\envs\deeplearning\Lib\site-packages\nnunet\run)**
- 

















download the zipped pakaged of STU-Net form https://github.com/uni-medical/STU-Net/tree/main
save in D:\deeplearning. and unzips it
download


