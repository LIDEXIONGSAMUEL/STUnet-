# STU-net/nnU-net for GPU turbo
- https://github.com/uni-medical/STU-Net

## Enviroment
-Windows 11

## requirement
- **anaconda** navigator download:(https://www.anaconda.com/download)
- **pycharm community editor**:(https://www.jetbrains.com/pycharm/download/?section=windows)
- **CUDA Toolkit 12.2 Downloads**(https://developer.nvidia.com/cuda-12-2-0-download-archive?target_os=Windows&target_arch=x86_64&target_version=11&target_type=exe_local)
- **cuDNN**(https://developer.nvidia.com/cudnn-downloads?target_os=Windows&target_arch=x86_64&target_version=Agnostic&cuda_version=12) and installation see details inhttps://blog.csdn.net/qlkaicx/article/details/134577555


## Edit the system enviroment variables
- add Variable:**CUDA_PATH**; Value:**C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.6**
- add Variable:**CUDA_PATH_V12_6**; Value:**C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.6**
- system variable--->Path(variable)--->edit:add **C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.6\bin** and **C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.6\libnvvp**
- add Variable:nnUNet_preprocessed; Value: D:\nnUNet_preprocessed
- add Variable:nnUNet_raw; Value: D:\nnUNet_raw
- add Variable:nnUNet_results: D:\nnUNet_results

## anaconda3
- Environment--->create--->python 3.12.8
- anaconda3 is a useful tool to create and manage python environmrnt, where my python environment is named **deeplearning**.
- 
### dependencies
- activate **your python**
- pip install batchgenerators (the cmd should show (deeplearning) C:\Users\admin>pip install batchgenerators :where (deeplearning is the name of python enviroment)
- pip install torchinfo
- pip install nibabel
- pip install tqdm
- pip install nnunet

## nnunet 1.7.1 modification 
- check the unzipped file named **nnUNet-1.7.1** download from **(https://github.com/uni-medical/STU-Net)**

- check the file: **(C:\Users\admin\anaconda3\envs\**deeplearning**\Lib\site-packages\nnunet)**

- copy file from **(STU-Net-main\nnUNet-1.7.1\nnunet\network_architecture)** to **(C:\Users\admin\anaconda3\envs\deeplearning\Lib\site-packages\nnunet\network_architecture)**

- copy file from **(STU-Net-main\nnUNet-1.7.1\nnunet\training\network_training)** to **(C:\Users\admin\anaconda3\envs\deeplearning\Lib\site-packages\nnunet\training\network_training)**
  
- copy python file from **(nnunet/run/run_finetuning.py)** to **(C:\Users\admin\anaconda3\envs\deeplearning\Lib\site-packages\nnunet\run)**
  ## Documentation
- cmd--->
- **set nnUNet_raw_data_base=D:\nnUNet_raw_data_base** and **set RESULTS_FOLDER=D:\RESULTS_FOLDER** (it is the temporary method to set up the path see details https://github.com/MIC-DKFZ/nnUNet/blob/master/documentation/setting_up_paths.md )
  
- create the path in sequence like this :RESULTS_FOLDER/nnUNet/3d_fullres/

```
- Task101_TotalSegmentator/
  - STUNetTrainer_small__nnUNetPlansv2.1/
    - plans.pkl
    - fold_0/
      - small_ep4k.model
      - small_ep4k.model.pkl
  - STUNetTrainer_base__nnUNetPlansv2.1/
    - plans.pkl
    - fold_0/
      - base_ep4k.model
      - base_ep4k.model.pkl
  - STUNetTrainer_large__nnUNetPlansv2.1/
    - plans.pkl
    - fold_0/
      - large_ep4k.model
      - large_ep4k.model.pkl
  - STUNetTrainer_huge__nnUNetPlansv2.1/
    - plans.pkl
    - fold_0/
      - huge_ep4k.model
      - huge_ep4k.model.pkl
```

## direct inference for STU-net

- activation the python 
- ![image](https://github.com/user-attachments/assets/0b91be1e-41e3-4da3-93c1-9895effae367)
- direct to the file where **direct_inference.py** exist
- ![image](https://github.com/user-attachments/assets/c7b5d3be-00b5-48c5-8a04-f187e6fe5c98)
- input (python direct_inference.py STUNetTrainer_base D:\deeplearning\STU-Net-main\direct_inference\example\Task032_AMOS22_Task1 D:\deeplearning\STU-Net-main\output_dir! )
- where STUNetTrainer_base is the trainer,
- D:\deeplearning\STU-Net-main\direct_inference\example\Task032_AMOS22_Task1 is the input file
- D:\deeplearning\STU-Net-main\output_dir! is the output file.






