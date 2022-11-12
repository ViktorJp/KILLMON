# KILLMON
KILLMON v0.1 - Asus-Merlin Kill Switch Monitor & Configurator by Viktor Jaep, 2022

KILLMON is a shell script that provides additional capabilities outside of the VPN kill switch functionality that is currently integrated into the Asus-Merlin Firmware. This script builds on the excellent kill switch functionality originally provided by @Eibgrad, and provides an interface to enable, disable kill switch operations, as well as allowing you to choose how to implement the kill switch. Currently, it provides capabilities for 3 different scenarios:

1) Paranoid mode - All LAN traffic is forbidden from using the current WAN interface
2) IP Range mode - All LAN traffic within specified IP Range is forbidden from using the current WAN interface
3) Single IP mode - ALL LAN traffic on specified IP is forbidden from using the current WAN interface

In each instance, a valid VPN tunnel must be up and running for traffic to make it out to the internet, preventing any possibly traffic leaks while a VPN tunnel is down, thus the necessity for a kill switch.

WARNING: Please note that if IPv6 is enabled on your router, any and all traffic that utilizes IPv6 addressing will be leaking traffic around your VPN tunnel. If the tunnel goes down, LAN clients will be able to make it outside your network over your WAN interface, even with this IPv4 kill switch in place. Recommend disabling IPv6 from the router interface itself until better capabilities present itself to prevent IPv6 leaks.
