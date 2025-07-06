# Ledvence-Smart-WiFi-E27-A60-Local-Control
I developed this script to easy control LEDVANCE E27 A60 WiFi Bulb using local network. It use tinytuya protocol 3.5

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
  --shade 2700K-6500K  Color temperature in Kelvin (DPS 23)
  --rgb R,G,B          RGB color (0-255 each)
  --saturation 1-100   Saturation for RGB (default: 100)
  --raw HHHHSSSSVVVV   12-digit hex HSV string (DPS 24)
  --debug              Enable verbose tinytuya logs (and fast test)
  --version            print utility version
adminpro@Admins-MacBook-Pro ~ % 
```
<br><br>
<h1>Tested on</h1>
Ledvance Smart+ WiFi E27 A60<br>
Main Module: V1.5.32<br>
MCU Module: V1.5.32<br>
RN bundle version: V1.3.0<br><br>
<h2>SMART+ WIFI CLASSIC 60 9 W/2700…6500 K E27 (MY)</h2>
<img src="https://www.ledvance.com/00_Free_To_Use/11536672/image-thumb__11536672__ProductGalleryImage/asset-11536672_SMARTWIFIA60_9W_230V_RGBWFR_E27_4X3LEDV.jpg" alt="bulb photo">
<a href="https://www.ledvance.com/en-int/home-lighting/products/smart-home/smart-lamps/smart-wifi/smart-classic-heatsink-lamps-with-wifi-technology/classic-bulb-shape-with-wifi-technology-c6443?productId=83025">https://www.ledvance.com/en-int/home-lighting/products/smart-home/smart-lamps/smart-wifi/smart-classic-heatsink-lamps-with-wifi-technology/classic-bulb-shape-with-wifi-technology-c6443?productId=83025</a>
