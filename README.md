
BECKOMBERGAVÄGEN 15
BROMMA,  168 54
(+46) 736 144 899
REACT.DEV.SE@GMAIL.COM     |  ![fb](https://github.com/iloveyii/iot-lab/blob/master/images/firebase1.png)
:-------------------------:|:-------------------------:
![fb](https://github.com/iloveyii/iot-lab/blob/master/images/firebase1.png)  |  ![ifttt](https://github.com/iloveyii/iot-lab/blob/master/images/ifttt1.png)
![fb](https://github.com/iloveyii/iot-lab/blob/master/images/html51.png)  |  ![ifttt](https://github.com/iloveyii/iot-lab/blob/master/images/js1.png)
![fb](https://github.com/iloveyii/iot-lab/blob/master/images/node1.png)  |  ![ifttt](https://github.com/iloveyii/iot-lab/blob/master/images/smarthome.jpg)
![fb](https://github.com/iloveyii/iot-lab/blob/master/images/thingy.jpg)  | ![fb](https://github.com/iloveyii/iot-lab/blob/master/images/hkr.png)   

## Installation
   * Clone repo `git clone https://github.com/iloveyii/iot-lab`
   * npm i --unsafe-perm
   * npm run task1 # 2,3...7
    
## Implementation

### OS install
  * Download Raspbian Buster with Desktop from `https://www.raspberrypi.org/downloads/raspbian/`.
  * Extract the image from the above step and write to SD card using Ubuntu Image Writer or Etcher.
  * In the boot partition of SD card `touch ssh` to enable ssh.
  * Auto connect to wifi, nano `/etc/wpa_supplicant/wpa_supplicant.conf` and add the following at the end
```bash
network={
   ssid="your-wifi"
   psk="your-wifi-password"
}
``` 
  * Eject SD card from computer and place in PI, power up PI.
  * To ssh to PI you need to find IP and may scan network by using `nmap -sS 192.168.0.0/24` or whatever is your network.
  * ssh pi@192.168.0.11, assuming this is your ip, default username is pi and password is raspberry. Change it by `sudo passwd pi`'
  * Install required packages `sudo apt install bluetooth bluez libbluetooth-dev libbluetooth-dev libudev-dev`
   
## Firebase functions
   * npm i -g firebase-tools
   * firebase login
   * firebase init functions
   * firebase deploy --only functions --debug

## SD card
   * Clone SD cards 
```bash
    sudo dd if=/dev/sda of=~/sda.img bs=4096 conv=notrunc,noerror status=progress
```
