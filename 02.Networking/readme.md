# Hands on Lab: Virtual network peering / Network security groups / User routes

You can connect virtual networks to each other with virtual network peering. These virtual networks can be in the same region or different regions (also known as Global VNet peering). Once virtual networks are peered, resources in both virtual networks are able to communicate with each other, with the same latency and bandwidth as if the resources were in the same virtual network. 

You can filter network traffic inbound to and outbound from a virtual network subnet with a network security group. Network security groups contain security rules that filter network traffic by IP address, port, and protocol. Security rules are applied to resources deployed in a subnet. 

Azure routes traffic between all subnets within a virtual network, by default. You can create your own routes to override Azure's default routing. The ability to create custom routes is helpful if, for example, you want to route traffic between subnets through a network virtual appliance (NVA).

## Exercises

1. [Virtual network peering](tutorial-connect-virtual-networks-portal.md)
2. [Filter network traffic with NSGs](tutorial-filter-network-traffic.md) 
3. [Set up custom routes](tutorial-create-route-table-portal.md)

## Remarks

To enable ip routing on Ubuntu, please use the following:

```
sudo sysctl -w net.ipv4.ip_forward=1
```
