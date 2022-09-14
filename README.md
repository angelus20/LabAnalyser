# LabAnalyser
A plugin based open source data modification and visualization tool

____________
____________

**Create editable variales (parameter) or data in a plugin (see https://github.com/ConverterLabs/PluginTemplate) and use the visualization of LabAnalyser.
Create UserInterfaces with QTCreator and connect them with the variables via drag and drop.**
![LabAnalyser](readme_pictures/show_variables.png)

____________
____________


**Use the signal slot system of qt in QTCreator to create sophisticated userinterfaces.**

![Stateflow visualisation](readme_pictures/UseQTCreator.png)

____________
____________


**Load as many UserInterfaces as needed to LabAnalyser. And visualize hundreds of thousands of data points in realtime**
![Array of windows on four screens](readme_pictures/UndockAndCreate_MonitorArray.png)

**Use features as export to HDF5 or Matlab-File (*.mat) so store the data. Or directly connect Matlab via TCP/IP.**
![Array of windows on four screens](readme_pictures/export.png)


____________
____________

## How to compile LabAnalyser 

### For Windows 
Use msys2, install necessary packages as flollows:

1. `pacman -Syuu`
2. `pacman -Syuu`
3. `pacman -Syuu`
4. `pacman -S mingw-w64-i686-qt`
5. `pacman -S mingw-w64-i686-qt-creator`
6. `pacman -S mingw-w64-x86_64-qt`
7. `pacman -S mingw-w64-x86_64-qt-creator`
8. `pacman -S mingw-w64-x86_64-boost`
9. `pacman -S mingw-w64-x86_64-highfive`
10. `pacman -S git`
11. clone https://github.com/EyNuel/matOut.git
12. use patch < ../../../build-patches/MatOut-0001-Changes-to-use-the-lib-in-LabAnalyser.patch
13. open MinGW-w64 32-Bit- or 64-Bit-Shell and call "qtcreator" 
14. open LabAnalyser.pro


### For Linux (tested on Arch Linux)

1. install boost-libs 
   - Arch Linux: `pacman -S boost-libs`
2. install HighFive
   - Arch Linux: install from AUR `yay -S highfive` or `yaourt -S highfive`
3. create build folder `mkdir build`
4. create libs folder build/libs/ `mkdir build/libs/`
5. `cd build/libs`
6. `clone https://github.com/EyNuel/matOut.git` 
7. `cd matOut`
8. `patch < ../../../build-patches/MatOut-0001-Changes-to-use-the-lib-in-LabAnalyser.patch`
9.  change folder to build: `cd ../../`
10. run qmake inside build: `qmake ../`
11. run make: `make`
12. if successful: execude LabAnalyser `./LabAnalyser`


