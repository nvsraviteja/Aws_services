# VPC (Virtual Private Cloud)
* It is a isolated network which allows users to launch aws resources in a secure and customizable virtual network.

# Importance of Networking
* Networking provides communicate between systems, services, applications for transferring data between them
* when it comes to cloud it provides connectivity for data transfer between services and ensure security
* Key features of Networking
    * Enables Communication
    * Provides Security
    * Scalable
    * High availability

# Components of VPC
* CIDR Block
* Subnet
* Route tables
* Internet Gateway
* Security Groups
* NAT (Network Available Translation) Gateway
* Network ALC (Access control list)
* VPC Peering
* VPC Connection
* Direct connect
* VPC Flow logs

# Default VPC vs Custom VPC
* Default VPC: when you create your new AWS account there will be default VPC in each regions and public subnet in each Availability zones which are launched automatically by AWS by this user can immediately launch AWS resources using a default VPC.

* Custom VPC: User needs to create a Custom VPC according to their specifications and requirements

# IPv4 vs IPv6
* IPv4 uses 32-bit IP address and it is in numeric dot-decimal notation eg:192.168.0.12
* IPv6 user 128-bit IP address and it is in alphanumeric hexadecimal notation eg: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

# CIDR Block
* Classless Inter Domain Routing is a method of allocating IP addresses in VPC
* It is used to define the range of IP addresses that a vpc uses for its subnets
* It is also used to allocate the IP addresses to the VPC which has resources
* CIDR has 2 components
    * Base IP
        * It is a general IP address eg: 192.168.0.0
    * Subnet mask
        * it defines that how many bits can change in an IP for eg: /0, /8, /16, /24.
* There is a simple formula used to find the subnet mask that is `2^n-1` by solving it you will get a number `"N"` then use this formula `32-(1-N)` you will get the subnet mask
* If I want to allocate 1 IP addresses then `2^1-1=2^0=1` so N is 1 now we calculate the value of subnet mask `32-(1-1)=32-0=32`the subnet mask value is 32 so the IP address will be 192.168.0.0/32 here the allocated IP range is 192.168.0.0 if you want to add 8 IPs then `2^8-1=2`
* CIDR block contains host portion and network portion 
    * Network Portion: It is a fixed portion of IP that remains same for all the resources in same network
        * eg: 192.168.0.0/24 then 192.168.0.* is the Network Portion which will be the same for all the resources 
    * Host Portion: It is a part of IP which is used to identify the individual resources in a same network 
        * eg: 192.168.0.0/24 then 192.168.0.* here * will be uniq for all the services in the network this is known as host portion

* IP address is divided into 4 octets if subnet mask is
    * /32 no octets changes
    * /24 last octet changes
    * /16 last 2 octets changes
    * /8 last 3 octets changes
    * /0 all octets changes

# Subnets
* Subnets are range of IP addresses within a VPC
* Subnets allows users to segment or divide the VPC into manageable parts and it improves network organization by which we can identify the resources easily 
* We can easily manage our infrastructure with the help of subnets
## Types of Subnets
* Private Subnet
    * the resources in this subnet cannot directly communicate with the internet.
    * to communicate with the internet we need to attach NAT Gateway (Network Address Translation) 
* Public Subnet
    * The resources in Public subnet can directly communicate with the internet.
    * Public subnet is used to store the resources which need internet access
    * IGW is attached to the VPC so that the instances/resources in public subnet can access the internet 
* Isolated Subnet
    * This is a subnet which has no access to internet not even via NAT gateway ot IGW
    * The resources in this subnet cannot have access to internet.
    * This is used for resources which should not be accessed through internet.
    * the resources in this subnet enables internal communication.

# Route Tables
* It contains some set of rules which are used to direct the incoming network traffic from Internet Gateway
* Rules contains how the traffic flows from one IP address (source) to another IP address (destination)
* The Route Tables are associated with one or more subnets in the vpc. the subnet must be associated to the route table.
* The Route Table consists of range of IP address (destination) and the target (resource)
## Types of Route Tables
* Main Route Table
    * every VPC comes with default route table i.e: Main Route Table
* Custom Route Table
    * when user creates a route table that is known as custom route table in this user can provide their specific rules.

# Subnet routing
* It is a process of directing the traffic between the subnets in a VPC

# VPC PEERING and VPC Connection
* 