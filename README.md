# Build VC4CL on Raspberrypi

## Pi Zero & Raspi OS Lite (Buster)

1. Download OS image from [this Link](https://downloads.raspberrypi.com/raspios_oldstable_lite_armhf/images/raspios_oldstable_lite_armhf-2023-05-03/2023-05-03-raspios-buster-armhf-lite.img.xz).
2. Setup Pi Zero.
3. Login to Pi Zero Shell.
4. Update packafe lists
   ```bash
   sudo apt update
   ```
5. change Swap size.
   ```bash
   sudo vi /etc/dphys-swapfile
   ...
   # CONF_SWAPSIZE=100 # <- comment out
   CONF_SWAPSIZE=2048 # <- Add line
   ...
   ```
   ```bash
   sudo service dphys-swapfile restart
   ```

5. clone this repository & change directory.
   ```bash
   git clone https://github.com/junkei-okinawa/VC4CL-integration-build.git
   cd VC4CL-integration-build
   ```
6. run build.sh
   ```bash
   ./build.sh
   ```
   
