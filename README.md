# azpanfw
01/26/22 marketplace template




Panfw - directions
Enable eth1/1- set interface type layer3, set VR to default, set to DHCP client & uncheck default gateway, commit then set sec zone to untrust.
Enable eth1/2- set interface type layer3, set VR to default, set to DHCP client & uncheck default gateway, commit then set sec zone to trust.
Edit VR and enter default route 0.0.0.0/0 to first ip add in Untrust subnet.  eg 10.1.0.1
Edit VR and enter default route 10.1.0.0/24 to first ip add in Untrust subnet.  eg 10.1.0.1




Run Pan templete, when finished click the redeploy

Change Vm Name, Subnet1Start Address, Subnet2Start Address, Public IP Address Name, and Public IPRG Name in Parameters

Change PIP to static if not already.  Disassociate and click up to Standard Sku.

Create ilb.
Add hp to tcp 22
Add BE pool to internal interfaces
Create lbr and select ha ports.

Create UDR to point to lb ip add.
