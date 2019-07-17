
# servers with NVIDIA GPUs

## [LINUX X64 (AMD64/EM64T) DISPLAY DRIVER](https://www.nvidia.com/Download/driverResults.aspx/148589/en-us)
 * Version:	430.34
 * Release Date:	2019.7.9 
 * get the driver 
 
```bash
wget http://us.download.nvidia.com/XFree86/Linux-x86_64/430.34/NVIDIA-Linux-x86_64-430.34.run
chmod 755 NVIDIA-Linux-x86_64-430.34.run
sudo ./NVIDIA-Linux-x86_64-430.34.run --no-opengl-files
```
 * re-install
 ```
 sudo service lightdm stop
 
 sudo nvidia-uninstall
 
 sudo ./NVIDIA-Linux-x86_64-430.34.run --no-opengl-files
 
 sudo service lightdm start
 ```
 

## [CUDA and cuDNN compatiblity](https://stackoverflow.com/questions/50622525/which-tensorflow-and-cuda-version-combinations-are-compatible)


| CUDA      |  cuDNN |  TensorFlow  | Python | 
| ------------- |:-------------:| :-----:|  :-----:|
| 9       |  7  |  1.5 ~ 1.12 | 3.3 ~ 3.6 |

* current versions
```
yyoo@omega:~$ cat /usr/local/cuda/version.txt
CUDA Version 9.0.176

yyoo@omega:~$ grep CUDNN_MAJOR -A 2 /usr/local/cuda/include/cudnn.h
#define CUDNN_MAJOR 7
#define CUDNN_MINOR 0
#define CUDNN_PATCHLEVEL 5
```

Use Tensorflow *1.10* with Python 3.6

