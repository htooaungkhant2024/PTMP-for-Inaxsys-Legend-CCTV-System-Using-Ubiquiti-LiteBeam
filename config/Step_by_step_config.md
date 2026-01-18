# ⚙️ Step-by-Step Configuration
## STEP 1: Physical Installation
Central Location

Connect ISP → Router

Connect Router → PoE Switch

Connect NVR → PoE Switch

Connect LiteBeam Master → PoE Switch (PoE)

Remote Locations

Mount LiteBeam Left & Right with clear line-of-sight

Connect LiteBeam → PoE injector

Connect PoE injector → PoE switch

Connect cameras → PoE switch

## STEP 2: Configure LiteBeam Master (Access Point)

Access device via browser (default 192.168.1.20)

Wireless Settings
Wireless Mode:     Access Point (PtMP)
SSID:              CAM-PtMP
Channel Width:     40 MHz
Frequency:         Clean / DFS channel
Security:          WPA2-AES
airMAX:            Enabled
Output Power:      Medium

Network Settings
Network Mode:      Bridge
IP Address:        192.168.0.2
Subnet Mask:       255.255.255.0
Gateway:           192.168.0.1
DNS:               8.8.8.8


✔ Apply and reboot

## STEP 3: Configure LiteBeam Stations (Left & Right)

Repeat for each station.

Wireless Settings
Wireless Mode:     Station
SSID:              CAM-PtMP
Security:          WPA2-AES
airMAX:            Enabled


Scan for AP

Select LiteBeam Master

Lock to AP

Network Settings
Network Mode:      Bridge
IP Address:        192.168.0.3 (Left)
IP Address:        192.168.0.4 (Right)
Gateway:           192.168.0.1


✔ Apply and reboot

## STEP 4: Wireless Alignment & Validation

Align antennas using alignment tool

Target signal strength: -55 to -65 dBm

CCQ: 90%+

Lock frequency after alignment

## STEP 5: Configure Inaxsys Legend Cameras

For each camera:

Network Settings
IP Mode:        Static
IP Address:     Assigned camera IP
Subnet Mask:    255.255.255.0
Gateway:        192.168.0.1
DNS:            8.8.8.8

Video Settings
Codec:          H.265
Resolution:     4MP / 8MP
Frame Rate:     15–20 FPS
Bitrate:        4–8 Mbps
Rate Control:   CBR

STEP 6: Configure NVR
Network
IP Address:     192.168.0.10
Gateway:        192.168.0.1

Camera Setup

Add cameras via ONVIF

Use static IP addresses

Verify live view and recording

STEP 7: Router Configuration

DHCP: Disabled or reserved range

NAT: Enabled

Firewall: Enabled

Optional: VPN for remote viewing

## 📊 Bandwidth Planning
Item	Value
Cameras	6
Avg Bitrate	6 Mbps
Total Traffic	~36 Mbps

LiteBeam AC throughput: 300+ Mbps

## 🔐 Security Best Practices

WPA2-AES wireless encryption

Strong passwords on all devices

Static IPs for cameras and radios

VPN instead of port forwarding

## ✅ Testing Checklist

Cameras reachable from NVR

Stable wireless links

Low latency (< 5 ms)

Recording & playback verified

🏁 Conclusion

This project demonstrates a production-ready PtMP wireless CCTV deployment, showcasing:

Wireless networking expertise

CCTV system integration

Ubiquiti airMAX configuration

Real-world field implementation
