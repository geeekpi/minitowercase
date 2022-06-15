# minitowercase
This repository is for mini tower case's OLED 0.96 screen 
## How to enable OLED 0.96
1. Turn on `i2c function` by using `sudo raspi-config` -> `interface options` -> `i2c` -> `enable` -> `yes`.
2. Check if the screen has been recognized by Raspberry Pi
```bash
i2cdetect -y 1 
```
if encount `command not found` error, please install `i2c-tools` by using `sudo apt update && sudo apt -y install i2c-tools`. <br>

3. Install dependencies libraries:
```bash
sudo apt -y install python3 python3-pip python3-pil libjpeg-dev zlib1g-dev libfreetype6-dev liblcms2-dev libopenjp2-7 libtiff5
```
4. Grant privilleges to user `pi`
```bash
sudo usermod -a -G gpio,i2c pi
```
5. Download sample code from this repo:
```bash
git clone https://github.com/rm-hull/luma.examples.git
cd luma.examples/
```
6. Install the dependencies
```bash
sudo -H pip3 install -e .
```
7. Entering into example folder and test it.
```bash
cd examples/
python3 sys_info.py
```
8. You should seen this screen on OLED:


