# KILLMON
KILLMON v0.5 - Asus-Merlin IP4/IP6 Kill Switch Monitor & Configurator by Viktor Jaep, 2022

KILLMON is a shell script that provides additional capabilities outside of the VPN kill switch functionality that is currently integrated into the Asus-Merlin Firmware. KILLMON builds on the excellent kill switch script originally provided by @Eibgrad, and provides a user interface to help monitor, enable, or disable kill switch operations, as well as allowing you to choose how to implement the kill switch for both IP4 and IP6 traffic. Currently, KILLMON provides traffic kill modes for 3 different scenarios...

1) Paranoid mode - All LAN traffic is forbidden from using the current WAN interface
2) IP Range mode - All LAN traffic within specified IP Range is forbidden from using the current WAN interface
3) Single IP mode - All LAN traffic on specified IP is forbidden from using the current WAN interface

In each instance, a valid VPN tunnel must be up and running for traffic to make it out to the internet, preventing any possible traffic leaks while a VPN tunnel is down, thus the necessity for a kill switch.

IMPORTANT NOTE: Many kill switches do not consider IP6, or recommend just completely disabling IP6 on the router itself. KILLMON may very well be one of the first kill switches that both embraces and kills the sh*t out of unwanted IP6 traffic when your VPN connection goes down. Please note that if IPv6 is enabled on your router and are using a kill switch of any kind that does not specifically block IP6, any and all traffic that utilizes IPv6 addressing will be leaking traffic around your IP4 VPN tunnel over your WAN when it goes down. 
