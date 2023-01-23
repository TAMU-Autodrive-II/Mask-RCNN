# <ins> About The Folders </ins>
The *cocoapi* directory contains data from another github [here](https://github.com/cocodataset/cocoapi) which contains a necessary setup step for successfully running the Mask-RCNN model.

The MaskRCNN directory contains data from a version of Mask-RCNN that has been modified to work with TensorFlow 2 [here](https://github.com/leekunhee/Mask_RCNN.git).

Additional light modifications have been made to get it to work on my system.
# <ins> Setup Instructions </ins>
## Below RTX 30 series
1.	Install Visual Studio Community (2017) and install the C++ development tools (include 2015 Build tools for cocoapi later) 
2.	[Install](https://developer.nvidia.com/cuda-toolkit-archive) Cuda Version  10.0, use the express installation option. 
3.	[Download](https://developer.nvidia.com/rdp/cudnn-archive) CuDNN version 7.4 and put the cudnn files in the lib, bin, and include folders into the lib, bin, and include folders of the Cuda installation (C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.0)
4.	Put the bin, libnvvp, and \extras\CUPTI\lib64 folders on the path. Ensure there is a CUDA_PATH and a CUDA_PATH_Vxx_x in your system variables.

## RTX 30 Series 
*This was done on a RTX 3060*
1.	Install Visual Studio Community (2019) and install the C++ development tools (include 2015 Build tools for cocoapi later)  
2.	[Install](https://developer.nvidia.com/cuda-toolkit-archive) Cuda Version  11.2, use the express installation option. 
3.	[Download](https://developer.nvidia.com/rdp/cudnn-archive) CuDNN version 8.1 and put the cudnn files in the lib, bin, and include folders into the lib, bin, and include folders of the Cuda installation (C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.1)
4.	Put the bin, libnvvp, and \extras\CUPTI\lib64 folders on the path. Ensure there is a CUDA_PATH and a CUDA_PATH_Vxx_x in your system variables

# <ins> Installation Steps </ins>
1.	Create a conda environment using python 3.8
2.	Install the packages outlined in the requirements.txt file (provided the previous setup steps are the same). 
3.	Go into the cocoapi folder and continue until you are in the PythonAPI directory
4.	Type “python setup.py build_ext install”
5.	Go back into the MRCNN root directory and use the same command. 

# <ins> Running Steps </ins>
To run, enter the Mask_RCNN/samples directoru and run the demo.py file. This is a simple demo that will output a result to the Results folder (its supposed to also have a popup but at this version that has not worked on my system)