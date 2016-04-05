# How to configure two NIC's with two gateways

Edit ```/etc/network/interfaces``` file as following

```
# Feel free to change IP and gateway    
# as per your local setup and routing   
# policy                                

# Setup the loopback network interface (lo0) 

auto lo
iface lo inet loopback

# Setup eth0 - connected to private LAN/VLAN 
auto eth0
allow-hotplug eth0
iface eth0 inet static
        address 10.70.201.5
        netmask 255.255.255.192
                                  # Ubuntu Linux add persistent route command
        post-up route add -net 10.0.0.0 netmask 255.0.0.0 gw 10.70.201.6


# Setup eth1 - connected to the Internet 
auto eth1
allow-hotplug eth1
iface eth1 inet static
        address 205.153.203.98
        netmask 255.255.255.248
                                # Ubuntu Linux - This is your default gateway 
        gateway 205.153.203.97
```
