# High-availability-network-foundation
Learning AWS architecture.
# Summary
#This phase establishes a logical isolation virtual network on AWS using Amazon VPC. The architecture is designed for High Availability (HA) and Zero-#Trust Security by separating public-facing entry points from private data tiers across multiple physical data centers (Availability Zones).

# Architecture Specifications.
# Component       Tecnical configuration                                           Nutrient Value.
 #VPC                  10.0.0.0/16                 Provides 65,536 private IP addresses. Ensures absolute isolation from the  public internet.

 #Public Subnets       10.0.1.0/24 (AZ-A)         High Availability uses two separate data center. These the "internet-facing" layer.
                      10.0.2.0/24 (AZ-B) 
                      
 #Private Subnets      10.0.10.0/24 (AZ-A)        Data Security, Completely isolated from the internet. Reserved for databases and sensitive logic.        #                      10.0.11.0/24 (AZ-B)

#Internet-Gateway       Attached                 Acts as the VPC's communication bridge to the public web.


 
# Routing Logic
#Public Route Table, maps 0.0.0.0/0 all local traffic to the internet gateway. Which transfor a standar subnet into a public subnet.
#Subnet Association, uses the links of a Public Route explicitly to connect with web subnets creating a two way comunicacion.


# Skills Demostraded:
#Networking: CIDR Math, Subnetting, Route Tables.
#Cloud Architecture: Multi-AZ Redundancy, Security Group Isolation.
