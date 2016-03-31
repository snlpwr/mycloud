# Glossary

### API

Application programming interface.

### API endpoint

The daemon, worker, or service that a client communicates with to access an API. API endpoints can provide any number of services, such as authentication, sales data, performance metrics, Compute VM commands, census data, and so on.

### bare 

An Image service container format that indicates that no container exists for the VM image.

### Block Storage

The OpenStack core project that enables management of volumes, volume snapshots, and volume types. The project name of Block Storage is cinder.

### CirrOS

A minimal Linux distribution designed for use as a test image on clouds such as OpenStack.

### cloud controller node

A node that runs network, volume, API, scheduler, and image services. Each service may be broken out into separate nodes for scalability or availability.

### Compute

The OpenStack core project that provides compute services. The project name of Compute service is nova.

### compute node 

A node that runs the nova-compute daemon that manages VM instances that provide a wide range of services, such as web applications and analytics.

### controller node

Alternative term for a cloud controller node.

### Database service

An integrated project that provide scalable and reliable Cloud Database-as-a-Service functionality for both relational and non-relational database engines. The project name of Database service is trove. 

### Data processing service

OpenStack project that provides a scalable data-processing stack and associated management interfaces. The code name for the project is sahara.

### DHCP

Dynamic Host Configuration Protocol. A network protocol that configures devices that are connected to a network so that they can communicate on that network by using the Internet Protocol (IP). The protocol is implemented in a client-server model where DHCP clients request configuration data, such as an IP address, a default route, and one or more DNS server addresses from a DHCP server.

### DHCP agent

OpenStack Networking agent that provides DHCP services for virtual networks.

### DNS

Domain Name Server. A hierarchical and distributed naming system for computers, services, and resources connected to the Internet or a private network. Associates a human-friendly names to IP addresses.

### dnsmasq

Daemon that provides DNS, DHCP, BOOTP, and TFTP services for virtual networks.

### domain

In the Identity service, provides isolation between projects and users.

On the Internet, separates a website from other sites. Often, the domain name has two or more parts that are separated by dots. For example, yahoo.com, usa.gov, harvard.edu, or mail.yahoo.com.

Also, a domain is an entity or container of all DNS-related information containing one or more records.

### extended attributes (xattr)

File system option that enables storage of additional information beyond owner, group, permissions, modification time, and so on. The underlying Object Storage file system must support extended attributes.

### external network

A network segment typically used for instance Internet access.

### firewall

Used to restrict communications between hosts and/or nodes, implemented in Compute using iptables, arptables, ip6tables, and etables.

### flat network

Virtual network type that uses neither VLANs nor tunnels to segregate tenant traffic. Each flat network typically requires a separate underlying physical interface defined by bridge mappings. However, a flat network can contain multiple subnets.

### floating IP address

An IP address that a project can associate with a VM so that the instance has the same public IP address each time that it boots. You create a pool of floating IP addresses and assign them to instances as they are launched to maintain a consistent IP address for maintaining DNS assignment.

### gateway

An IP address, typically assigned to a router, that passes network traffic between different networks.

### generic receive offload (GRO)

Feature of certain network interface drivers that combines many smaller received packets into a large packet before delivery to the kernel IP stack.

### generic routing encapsulation (GRE)

Protocol that encapsulates a wide variety of network layer protocols inside virtual point-to-point links. 

### hypervisor

Software that arbitrates and controls VM access to the actual underlying hardware.

### IaaS

Infrastructure-as-a-Service. IaaS is a provisioning model in which an organization outsources physical components of a data center, such as storage, hardware, servers, and networking components. A service provider owns the equipment and is responsible for housing, operating and maintaining it. The client typically pays on a per-use basis. IaaS is a model for providing cloud services.

### ICMP

Internet Control Message Protocol, used by network devices for control messages. For example, ping uses ICMP to test connectivity.

### Identity Service

The OpenStack core project that provides a central directory of users mapped to the OpenStack services they can access. It also registers endpoints for OpenStack services. It acts as a common authentication system. The project name of the Identity Service is keystone.

### Image service

An OpenStack core project that provides discovery, registration, and delivery services for disk and server images. The project name of the Image service is glance.

### instance

A running VM, or a VM in a known state such as suspended, that can be used like a hardware server.

### instance tunnels network

A network segment used for instance traffic tunnels between compute nodes and the network node.

### interface

A physical or virtual device that provides connectivity to another device or medium.

### Internet protocol (IP)

Principal communications protocol in the internet protocol suite for relaying datagrams across network boundaries.

### ipset

Extension to iptables that allows creation of firewall rules that match entire "sets" of IP addresses simultaneously. These sets reside in indexed data structures to increase efficiency, particularly on systems with a large quantity of rules.

### iptables

Used along with arptables and ebtables, iptables create firewalls in Compute. iptables are the tables provided by the Linux kernel firewall (implemented as different Netfilter modules) and the chains and rules it stores. Different kernel modules and programs are currently used for different protocols: iptables applies to IPv4, ip6tables to IPv6, arptables to ARP, and ebtables to Ethernet frames. Requires root privilege to manipulate.

### iSCSI

The SCSI disk protocol tunneled within Ethernet, supported by Compute, Object Storage, and Image service.

### jumbo frame

Feature in modern Ethernet networks that supports frames up to approximately 9000 bytes.

### kernel-based VM (KVM)

An OpenStack-supported hypervisor. KVM is a full virtualization solution for Linux on x86 hardware containing virtualization extensions (Intel VT or AMD-V), ARM, IBM Power, and IBM zSeries. It consists of a loadable kernel module, that provides the core virtualization infrastructure and a processor specific module. 

### Layer-3 (L3) agent

OpenStack Networking agent that provides layer-3 (routing) services for virtual networks.

### load balancer

A load balancer is a logical device that belongs to a cloud account. It is used to distribute workloads between multiple back-end systems or services, based on the criteria defined as part of its configuration.

### Logical Volume Manager (LVM)

Provides a method of allocating space on mass-storage devices that is more flexible than conventional partitioning schemes.

### management network

A network segment used for administration, not accessible to the public Internet.

### maximum transmission unit (MTU)

Maximum frame or packet size for a particular network medium. Typically 1500 bytes for Ethernet networks.

### message queue

Passes requests from clients to the appropriate workers and returns the output to the client after the job completes.

### Metadata agent

OpenStack Networking agent that provides metadata services for instances.

### multi-host

High-availability mode for legacy (nova) networking. Each compute node handles NAT and DHCP and acts as a gateway for all of the VMs on it. A networking failure on one compute node doesn't affect VMs on other compute nodes.

### Network Address Translation (NAT)

The process of modifying IP address information while in transit. Supported by Compute and Networking.

### Network Time Protocol (NTP)

A method of keeping a clock for a host or node correct through communications with a trusted, accurate time source.

### Networking

A core OpenStack project that provides a network connectivity abstraction layer to OpenStack Compute. The project name of Networking is neutron.

### Object Storage

The OpenStack core project that provides eventually consistent and redundant storage and retrieval of fixed digital content. The project name of OpenStack Object Storage is swift.

### Open vSwitch

Open vSwitch is a production quality, multilayer virtual switch licensed under the open source Apache 2.0 license. It is designed to enable massive network automation through programmatic extension, while still supporting standard management interfaces and protocols (for example NetFlow, sFlow, SPAN, RSPAN, CLI, LACP, 802.1ag). 

### OpenStack

OpenStack is a cloud operating system that controls large pools of compute, storage, and networking resources throughout a data center, all managed through a dashboard that gives administrators control while empowering their users to provision resources through a web interface. OpenStack is an open source project licensed under the Apache License 2.0.

### Orchestration

An integrated project that orchestrates multiple cloud applications for OpenStack. The project name of Orchestration is heat.

### path MTU discovery (PMTUD)

Mechanism in IP networks to detect end-to-end MTU and adjust packet size accordingly.

### plug-in

Software component providing the actual implementation for Networking APIs, or for Compute APIs, depending on the context.

### project

A logical grouping of users within Compute; defines quotas and access to VM images.

### promiscuous mode

Causes the network interface to pass all traffic it receives to the host rather than passing only the frames addressed to it.

### public key authentication

Authentication method that uses keys rather than passwords.

### QEMU Copy On Write 2 (QCOW2)

One of the VM image disk formats supported by Image Service.

### Quick EMUlator (QEMU)

QEMU is a generic and open source machine emulator and virtualizer.

One of the hypervisors supported by OpenStack, generally used for development purposes.

### RESTful

A kind of web service API that uses REST, or Representational State Transfer. REST is the style of architecture for hypermedia systems that is used for the World Wide Web.

### role

A personality that a user assumes to perform a specific set of operations. A role includes a set of rights and privileges. A user assuming that role inherits those rights and privileges.

### router

A physical or virtual network device that passes network traffic between different networks.

### security group

A set of network traffic filtering rules that are applied to a Compute instance.

### service

An OpenStack service, such as Compute, Object Storage, or Image Service. Provides one or more endpoints through which users can access resources and perform operations.

### subnet

Logical subdivision of an IP network.

### Telemetry

An integrated project that provides metering and measuring facilities for OpenStack. The project name of Telemetry is ceilometer.

### tenant

A group of users; used to isolate access to Compute resources. An alternative term for a project.

### user

In Identity Service, each user is associated with one or more tenants, and in Compute can be associated with roles, projects, or both.

### virtual extensible LAN (VXLAN)

A network virtualization technology that attempts to reduce the scalability problems associated with large cloud computing deployments. It uses a VLAN-like encapsulation technique to encapsulate Ethernet frames within UDP packets.

### virtual machine (VM)

An operating system instance that runs on top of a hypervisor. Multiple VMs can run at the same time on the same physical host.

### virtual networking

A generic term for virtualization of network functions such as switching, routing, load balancing, and security using a combination of VMs and overlays on physical network infrastructure. 

### Virtual Network Computing (VNC)

Open source GUI and CLI tools used for remote console access to VMs. Supported by Compute.

### virtual private network (VPN)

Provided by Compute in the form of cloudpipes, specialized instances that are used to create VPNs on a per-project basis.

### VLAN network

The Network Controller provides virtual networks to enable compute servers to interact with each other and with the public network. All machines must have a public and private network interface. A VLAN network is a private network interface, which is controlled by the vlan_interface option with VLAN managers.

### XFS

High-performance 64-bit file system created by Silicon Graphics. Excels in parallel I/O operations and data consistency.
