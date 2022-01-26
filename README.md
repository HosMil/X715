# X715

The PWN fan is not rotating when X715 is connected to PI 4, we need to to install the pwm fan control script

The pytone file need pigpiod library, so we need to install it firstly.


2022_01_26

LLine number 15 and 16 do not perform the packages are installed after the upgrade. RPi only uses Python3.

Do a check first using Python -V , Python3 -V and PIP --version and PIP3 --version.

```
sudo apt-get install -y pigpio python-pigpio python3-pigpio
sudo systemctl enable pigpiod
git clone https://github.com/geekworm-com/x715
sudo reboot

cd ~
python /home/pi/x715/pwm_fan_control.py&
```
