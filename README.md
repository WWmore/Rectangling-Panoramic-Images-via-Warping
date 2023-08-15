# Rectangling-Panoramic-Images-via-Warping

Code of the paper: Kaiming He, Huiwen Chang, Jian Sun. Rectangling panoramic images via warping. SIGGRAPH, 2013.

Successfully works in Windows system.

## Installation
Refer https://code.visualstudio.com/docs/cpp/config-mingw
1. install MinGW (the sourse code is run in Linux, below is to run in Windows)
2. Add path C:\msys64\mingw64\bin
3. Check gcc, g++, gdb version (must work)
3. In main.cpp: set the input panorama image, and saved path for output rectangular panorama image
4. In main.cpp: Run C/C++ File
5. Double click execute.bat file


## Forked: 
1. 运行main.cpp即可将输入的不规则全景图片矩形化。
2. add_seam.hpp:该程序运用seam carving算法完成图片的初次变形，用动态规划算法找出一小块子图像中能量最小的缝隙进行图片resize，记录每个像素的位移量。
3. global_warp.hpp:利用seam carving得到的位移量计算原图像的grid mesh，运用warping的算法实现图像全局扭曲。
