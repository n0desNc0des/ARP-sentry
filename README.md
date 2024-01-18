# ARP-sentry

A Python script for detecting ARP spoofing attacks using Scapy.

## Usage

1. Place the script in the startup folder to run when the system boots.

2. Move the script to `/etc/init.d/` and make it executable:
   ```bash
   sudo mv script.py /etc/init.d/
   sudo chmod 755 /etc/init.d/script.py
Register the script to be run at startup:

sudo update-rc.d script defaults
Ensure the script is monitoring the desired network interface (e.g., wlan0):

sniff("wlan0")
Note
The script uses Scapy to sniff ARP packets and detect ARP spoofing attacks.
If an ARP response is received from a different MAC address than the actual MAC associated with the IP, it indicates a potential ARP spoofing attack.
Disclaimer
This tool is intended for educational and ethical use only. Ensure compliance with legal regulations and obtain proper authorization before using it in any environment.
