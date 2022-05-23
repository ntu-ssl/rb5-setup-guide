# rb5-setup-guide

For more details, please checkout the following website:

- [Linaro Official Page](http://releases.linaro.org/96boards/rb5/linaro/debian/21.12/)
- [96boards Installation Guide](https://www.96boards.org/documentation/consumer/dragonboard/qualcomm-robotics-rb5/installation/) - [Installation with Linux Host](https://www.96boards.org/documentation/consumer/dragonboard/qualcomm-robotics-rb5/installation/linux-fastboot.md.html), [Download bootloader and OS image](https://www.96boards.org/documentation/consumer/dragonboard/qualcomm-robotics-rb5/downloads/)

## A video about how to get in fastboot mode

[Video](fastboot_mode.mp4)

## My environment

5.11.0-46-generic #51~20.04.1-Ubuntu x86_64

## Set up Guide

1. Install needed packages on Linux Host

    ```bash
    sudo apt-get update -y
    sudo apt install android-tools-fastboot # For Fastboot
    sudo apt install android-tools-mkbootimg # For making custom image
    sudo apt-get install gcc-aarch64-linux-gnu # For cross compiling
    ```

2. Connect host computer to RB5
   - RB5 must be powered off (unplugged from power)
   - please check the Quick start guide to set the dip switches on the development kit

3. Boot RB5 into fastboot mode  
    **Please read all bullet points before attempting**
    - Disconnect the power cable from the board and make sure no USB cable is plugged into the board
    - Hold down the “VOL-“ button while reconnecting the power supply.
    - Tap the “ON/OFF” button while continuing to hold the “VOL-“ button for ~5 seconds.
    - Release “VOL-“ button
    - Connect the USB3 Type C between the Linux PC and the board
    - Board should boot into fastboot mode

4. From the connected host machine terminal window, run the following commands to make sure device is connected and in fastboot mode
![check_success.png](https://i.imgur.com/zm3iPEa.png)

5. Following the guide from [linaro](https://releases.linaro.org/96boards/rb5/linaro/debian/21.12/) (The **Running the Developer based image** part)

![](https://i.imgur.com/QRY6DAf.png)
