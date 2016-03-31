# How to configure Network Time Protocol

## Controller Node
  1. To nstall ntp service
  
  ```# apt-get install ntp```

  2. To configure the NTP service
  
  By default, the controller node synchronizes the time via a pool of public servers. However, you can optionally edit the ```/etc/ntp.conf``` file to configure alternative servers such as those provided by your organization.
  
  Edit the ```/etc/ntp.conf``` file and add, change, or remove the following keys as necessary for your environment:
  ```
  server NTP_SERVER iburst
  restrict -4 default kod notrap nomodify
  restrict -6 default kod notrap nomodify
  ```
  Replace NTP_SERVER with the hostname or IP address of a suitable more accurate (lower stratum) NTP server. The configuration supports multiple server keys.
  
    __Note:__ For the restrict keys, you essentially remove the nopeer and noquery options.
  
    __Note:__ Remove the ```/var/lib/ntp/ntp.conf.dhcp``` file if it exists.
  
  3. Restart the NTP service:
  
  ```# service ntp restart```
  
  
## Other Nodes
  1. To install the NTP service
  
    ```# apt-get install ntp```

  2. To configure the NTP service
  
    Configure the network, compute, block and object nodes to reference the controller node.
    
    Edit the ```/etc/ntp.conf``` file:

    Comment out or remove all but one server key and change it to reference the controller node.
    
    ```server controller iburst```
    
    __Note:__ Remove the ```/var/lib/ntp/ntp.conf.dhcp``` file if it exists.
  
  3. Restart the NTP service:
    
    ```# service ntp restart```

## Verify operation
  
 It is recommended that you verify NTP synchronization before proceeding further. Some nodes, particularly those that reference the controller node, can take several minutes to synchronize.
 
 1. Run this command on the controller node:

    ```
    sunil@controller:~$ ntpq -c peers
    remote           refid      st t when poll reach   delay   offset  jitter
    ==============================================================================
    *125.62.193.121  129.6.15.29      2 u  563 1024  377   60.920   18.894   2.531
    +123.108.200.124 103.51.222.210   4 u  464 1024  377   61.039  -23.212   5.794
    +juniperberry.ca 193.79.237.14    2 u 1537 1024   36  129.619  -11.896   2.762
    ```

   Contents in the remote column should indicate the hostname or IP address of one or more NTP servers. 
    
    __Note:__ Contents in the refid column typically reference IP addresses of upstream servers.

 2. Run this command on the controller node: 

    ```
    sunil@controller:~$ ntpq -c assoc
    ind assid status  conf reach auth condition  last_event cnt
    ===========================================================
    1 28606  963a   yes   yes  none  sys.peer    sys_peer  3
    2 28607  943a   yes   yes  none candidate    sys_peer  3
    3 28608  9424   yes   yes  none candidate   reachable  2
    ```
    
    Contents in the condition column should indicate sys.peer for at least one server.

 3. Run this command on all other nodes:

  ```
  sunil@compute1:~$ ntpq -c peers
  remote           refid      st t when poll reach   delay   offset  jitter
  ==============================================================================
  *controller 125.62.193.121   3 u  664 1024  377    0.242   -2.106   0.202
  ```
  
  Contents in the remote column should indicate the hostname of the controller node.

  __Note:__ Contents in the refid column typically reference IP addresses of upstream servers.
  
 4. Run this command on all other nodes: 
  
  ```
  sunil@compute1:~$ ntpq -c assoc
  ind assid status  conf reach auth condition  last_event cnt
  ===========================================================
  1 46851  965a   yes   yes  none  sys.peer    sys_peer  5
  ```
  
  Contents in the condition column should indicate sys.peer.
