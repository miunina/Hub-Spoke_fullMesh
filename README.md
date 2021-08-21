# PFE2020MasterRSD
![topology](https://user-images.githubusercontent.com/49697768/129991006-23381140-8dd9-4b98-8b49-250462453056.png)

This is a collection of files that may helps to configure this hub & spokes topology in a way that the traffic will go through a mesh circuit. which means we are trying to configure the addvpn + sd-wan using fortigate firewall and cisco ios router.
```diff
@@"code", "cisco_vios_router", "cisco_vios_switch" branches :@@
step 0: configuring the WAN, LAN, vLANS, and VLAN grouping in zones, as well as the remote sites configurations separately is already done.
```diff
@@"code ADVPN_BGP_IPSec" branch :@@
step 1: 2 phases of IPSec VPN (Auto discovery sender enable) of Hub 1 (on 1 single fortigate) and the 2 spokes of the topology.
Each spoke contains 2 entries one spokeN° the other spokeN°_backup. Each must have a remote gateway. 

step 2: configure the necessary firewall policies.

step 3: Assign the IP address of the IPSec VPN interfaces (give the ip and remote-ip of the advpn_Hub and the spokeN° and spokeN°_backup).
Here normally advpns tunnels should be built.

Step 4: BGP configuration

Translated with www.DeepL.com/Translator (free version)
