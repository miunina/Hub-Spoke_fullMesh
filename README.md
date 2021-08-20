# PFE2020MasterRSD

IN THE END OF THE CONFIGURATIONS STEPS :
the ping from the pc in spoke 2 should ping to the spoke 3 ;

SOME OTHER CONFIGURATION SHOULD BE DONE ON THE GUI FORTIGATE:
1-dhcp server should be enabled in each vlan on the int of FW.
2- VLANs might be grouped in one internal lan (beta_lan, teta_lan, alpha_lan,internal_lan) , the intra-zone traffic shouldn't be blocked.
3- policies should be created using the zones created to allow traffic exchange (they should be in the end of the policies list).
4- configure interfaces on each ISP router.
