# LibArgus-oneShot-sample

## Description
The purpose of this repository is to show you how to use the NVIDIA LibArgus API with the most simple way in the Jetson board by using only one g++ command line to compile the oneShot sample which is included on /jetson_multimedia_api/argus/samples/oneShot without having your workspace set up inside the nested directories.

## How does this sample work?
1. Copy the script main.cpp included in this repository on your home directory
2. Install the tergra multimedia API if it's not already installed, this latter can be installded with the Jetpack or by the following CLI :

	`sudo apt install nvidia-l4t-jetson-multimedia-api`
3. Copy the jetson_multimedia_api folder in your home directory 
   `sudo cp /usr/src/jetson_multimedia_api/ $HOME`
4. Compile and run the sample

  ```
  $ g++ *.cpp -o oneShot -I jetson_multimedia_api/argus/include -L /usr/lib/aarch64-linux-gnu/tegra -lnvargus_socketclient
  $ ./oneShot
  ```
  Output :
  
  ```
  Argus Version: 0.97.3 (multi-process)
  PRODUCER: Available Sensor modes :
  PRODUCER: [0] W=3840 H=2160
  Wrote file: argus_oneShot.jpg
  ```

