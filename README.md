# Ledvence-Smart-WiFi-E27-A60-Local-Control

<h1>Dependencies</h1><br>
pip 25.1.1, python 3.11 (or newer)<br>
<b>TinyTuya version: 1.17.2</b><br>
<br>

Install TinyTuya:
```
pip install tinytuya
```
<br>

Scan local network for tuya devices
```
python -m tinytuya scan
```
<i>But it's easier to recognize it in LEDVANCE app</i>

<hr>

<h1>Tested on</h1>
Ledvance Smart+ WiFi E27 A60<br>
Main Module: V1.5.32<br>
MCU Module: V1.5.32<br>
RN bundle version: V1.3.0<br><br>

<hr>

<h1>Usage</h1>
LedvanceE27A60.py DEV_ID IP LOCAL_KEY [options]<br><br>

Example: 
```
python LedvanceE27A60.py a1b2c3d4e5f6g7h8ijklmn 192.168.0.238 'WQ!zYx8#kLp3vBn@' --tail
```
<br><br>

Help: 
```
adminpro@Admins-MacBook-Pro ~ % python LedvanceE27A60.py --help                                                                              
usage: LedvanceE27A60.py [-h] [--on | --off] [--status] [--tail [SEC]] [--brightness 1-100] [--shade 2300K-9000K] [--rgb R,G,B] [--saturation 1-100] [--raw HHHHSSSSVVVV] [--debug] [--version] dev_id ip local_key

CLI utility for Ledvance Smart+ E27 A60 RGBW lamp (Tuya protocol 3.5).
Tested on:
  Ledvance Smart+ WiFi E27 A60
  Main Module: V1.5.32
  MCU Module: V1.5.32
  RN bundle version: V1.3.0

USAGE (first 3 arguments are mandatory):
  LedvanceE27A60.py DEV_ID IP LOCAL_KEY [options]
  Example: python LedvanceE27A60.py a1b2c3d4e5f6g7h8ijklmn 192.168.0.238 'WQ!zYx8#kLp3vBn@' --tail

Version: 0.1

positional arguments:
  dev_id               Device ID
  ip                   Local IP Address
  local_key            Local Key

options:
  -h, --help           show this help message and exit
  --on                 Turn on the bulb (DPS 20)
  --off                Turn off the bulb (DPS 20)
  --status             Print current device status
  --tail [SEC]         Continuously print status every SEC (default: 1)
  --brightness 1-100   print utility version
  --shade 2300K-9000K  Color temperature in Kelvin (DPS 23)
  --rgb R,G,B          RGB color (0-255 each)
  --saturation 1-100   Saturation for RGB (default: 100)
  --raw HHHHSSSSVVVV   12-digit hex HSV string (DPS 24)
  --debug              Enable verbose tinytuya logs (and fast test)
  --version            print utility version
adminpro@Admins-MacBook-Pro ~ % 
```
