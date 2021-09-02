# Pre-configuration ADVPN+BGP on HUB & SPOKE


![topology_single_dual_homed_hub_and_spoke](https://github.com/miunina/Hub-Spoke_fullMesh/blob/miunina-patch-1/topology_single_dual_homed_hub_and_spoke.png)


This is a collection of files that may helps to configure this hub & spokes topology in a way that the traffic will go through a mesh circuit. which means we are trying to configure the addvpn + sd-wan using fortigate firewall and cisco ios router.
```diff
@@ "cisco_vios_router", "cisco_vios_switch" branches :@@
step 0: configuring the switches and routers (creating vlans, intervlans, enabling dhcp...).
```diff
@@"code CODE" branch :@@
In each file ("hub1.conf","spoke2.conf","spoke3.conf") we may find the necessary configuration which could be denoted and organized in steps as below: 
step 1: configure the interfaces , vlans, and static route to the networks connected to the IPSs

step 2: configure phase 1 and phase 2 of IPSec VPN (Auto discovery sender enable) of Hub 1 (on 1 single fortigate) and the 2 spokes of the topology.
Each spoke contains 2 entries one spokeN° the other spokeN°_backup. Each must have a remote gateway. 

step 3: Assign the IP address of the IPSec VPN interfaces (give the ip and remote-ip of the advpn_Hub and the spokeN° and spokeN°_backup).
Here normally advpns tunnels should be built.

step 4: configure thee dhcp

Step 5: BGP configuration

Step 6: configure the SD WAN , by creating an Load balancing sharing traffic among interfaces is based on SLA target.

step 7: configure the necessary firewall policies.
