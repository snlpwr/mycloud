# VJTICloud
VJTICloud is the private cloud build for [Veermata Jijabai Technological Institute](http://www.vjti.ac.in/). 
## Table of contents
* [What is cloud?](#what-is-cloud)
* [Service models of cloud](#Service-models-of-cloud)
  * [Software as a Service](#Software-as-a-Service)
  * [Platform as a Service](#Platform-as-a-Service)
  * [Infrastructure as a Service](#Infrastructure-as-a-Service)
* [Deployment models of cloud](#deployment-models-of-cloud)
  * [Public cloud](#public-cloud)
  * [Private cloud](#private-cloud)
  * [Hybrid cloud](#hybrid-cloud)
  * [Other](#Other)
    * [Community cloud](#Community-cloud)
    * [Intercloud](#Intercloud)
    * [Multicloud](#Multicloud)
    * [Distributed cloud ](#Distributed-cloud)


## What is cloud?
* Characteristics
    * Five essential characteristics
      * On demand service
      * Resource pooling
      * Measured service
      * Rapid elasticity and expansion
      * Broad network access
    * Other characteristics
      * Device and location independance
      * Reliability 
      * Productivity
      * Multitenancy
      * Maintenance
* Advantages
    * Work from anywhere
    * Flexibility
    * Automatic software updates
    * Increased collaboration
    * Capital expenditure free
    * Document control
    * Security
    * Competitiveness
    * Environmentally friendly
    * Disaster recovery 
    * Quick deployment


## Service models of cloud
 * ### Software as a Service

   Cloud services provided as an application.
 * ### Platform as a Service

   Development tools are provided through cloud.

 * ### Infrastructure as a Service

   VM's are given to user.


## Deployment models of cloud
  * ### Public cloud
 
    Availabe to general public for free or subscription basis.
  * ### Private cloud
 
    Build for private use by an organization.
  * ### Hybrid cloud

    Combination of public and private cloud.
  * ### Other

    * #### Community cloud


    * #### Intercloud


    * #### Multicloud


    * #### Distributed cloud


/etc/network/interfaces 
```
# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

# The loopback network interface
auto lo
iface lo inet loopback

auto p5p1
iface p5p1 inet dhcp

auto p5p1:0
iface p5p1:0 inet static
	address 10.0.0.31
	network 10.0.0.0
	netmask	255.255.255.0

auto p5p1:1
iface p5p1:1 inet static
	address 10.0.1.31
	network 10.0.1.0
	netmask 255.255.255.0

auto p5p1:2
iface p5p1:2 inet static
	address 10.0.2.31
	network 10.0.2.0
	netmask 255.255.255.0

```
Diagram

```
+--------------+ +--------------+
|  Controller  | |  Compute1    |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
|              | |              |
+--------------+ +--------------+

```
