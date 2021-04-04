## intro
hi everyone , a very good  _________ to all 
today i would like to welcome you all to the presentation on the topic 
Highly available AWS vpc architecture 

## pandemic
as now we are facing a pandemic situation we have to maintain a private space with proper distance even in public 
Similarly the organisations wants to maintain a private sanitised network in the public space of the AWS services and 
by keeping there data and databases private .

and this are achieved by a aws service known as VPC 
where we can define our own network and use all the aws services in our private space

## vpc
so a vpc is defined in a region OF AWS and can be spread in all the AZ. 
as per the definition we can now understand that ......................

## regions
AWS has the concept of a Region, which is a physical location around the world where we cluster data centers. We call each group of logical data centers an Availability Zone. Each AWS Region consists of multiple, isolated, and physically separate AZ's within a geographic area.
 Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks. AWS customers focused on high availability can design their applications to run in multiple AZ's to achieve even greater fault-tolerance.

## AZ
 An Availability Zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity in an AWS Region. AZs give customers the ability to operate production applications and databases that are more highly available, fault tolerant, and scalable than would be possible from a single data center. All AZs in an AWS Region are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZs. All traffic between AZs is encrypted.

## IP address
ip address or internet protocal address is simple label assigned as a unique entity to each device in a network. It is used to locate the host in a network through network ID . it is just similar to the emoplyee ID a unique id provided to all of us inside xebia.

## cidr notations
now lets come to another important topic CIDR notation 
classless inter domain routing  - helps us to reduce the wastage of ip address by providing exact number of ip address to the users.  with a special notation /n which specify number of bits present in network id

## route tables
 The place where routing information is stored is called a routing table. Routing table contains routing entries, that is list of destinations (often called: list of network prefixes or routes). ... Having the destination IP of packet, routers always choose best matching ROUTING ENTRY.

 route tables are set of rules which are used to determine where the network taffic has to be routed.  It specifies the destination subnet and the gateways or routers to reach it .

## internet gateway

 its a vpc component that helps instances to communicate over the internet using targets provided in the route table.

 # nat gateway
 a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances.

 To create a NAT gateway, you must specify the public subnet in which the NAT gateway should reside. For more information about public and private subnets, see Subnet routing. You must also specify an Elastic IP address to associate with the NAT gateway when you create it. The Elastic IP address cannot be changed after you associate it with the NAT Gateway.

 ## security groups and nacls

NACL stands for Network Access Control Lists. It is a security layer for your VPC that controls the traffic in and out of one or more subnets. It is an optional layer for your VPC. You can set up a Network ACL similar to the security group that adds an additional layer of security to your VPC.
