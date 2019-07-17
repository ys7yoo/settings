
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
 
