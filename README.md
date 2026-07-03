# ccna-branch-office-lab
Cisco Packet Tracer branch office network demonstrating OSPF, DHCP, SSH, NAT/PAT, EtherChannel and Cisco IOS configuration.
CCNA Branch Office Network Lab Walkthrough

Project Overview

For this project I built a small branch office network in Cisco Packet
Tracer. The goal was to practice several CCNA topics in one lab instead
of configuring each feature separately. By the end of the lab, both
branch networks could communicate with each other and reach a simulated
outside network.

Step 1 - Build the Topology

I started by placing three routers, two switches, six PCs, and one
server into Packet Tracer. After that I renamed each device so it was
easier to identify while configuring the network.

Step 2 - Connect the Devices

Next, I connected the routers, switches, PCs, and server with the
correct Ethernet cables. I also added two links between the switches so
I could configure an EtherChannel later in the lab.

Step 3 - Configure IP Addressing

I assigned IP addresses to every router interface and planned separate
subnets for each LAN and the WAN links. This made it easier to configure
routing later.

Step 4 - Configure the Router Interfaces

I configured each router interface with an IP address, added
descriptions, and enabled the interfaces with the no shutdown command. I
checked my work with show ip interface brief.

Step 5 - Configure DHCP

Instead of assigning addresses manually, I created DHCP pools on the
branch routers. The PCs were then set to obtain an IP address
automatically.

Step 6 - Configure OSPF

After the interfaces were working, I configured OSPF on all three
routers. This allowed the routers to learn routes dynamically instead of
using static routes.

Step 7 - Configure SSH

I configured SSH so the routers could be managed securely. I created a
local user account, generated RSA keys, and verified that I could log in
remotely.

Step 8 - Configure NAT/PAT

I configured PAT on the Branch-A router so devices on the private
network could reach the simulated outside network using one
public-facing address.

Step 9 - Configure EtherChannel

I bundled the two switch links into a single EtherChannel using LACP.
After that I verified that the port channel was up and forwarding
traffic.

Step 10 - Test the Network

I tested the network by pinging between the branch PCs, routers, and the
simulated Internet server. I also checked that DHCP, OSPF, NAT, and SSH
were all working correctly.

Step 11 - Verify the Configuration

Finally, I used commands like:

-   show ip route
-   show ip ospf neighbor
-   show ip nat translations
-   show etherchannel summary


to verify that everything was working as expected.

What I Learned

This lab helped me get more comfortable configuring routers and switches
using the Cisco CLI. It also gave me more practice with routing,
switching, DHCP, NAT, SSH, EtherChannel, and troubleshooting. Building
everything into one project helped me understand how these technologies
work together in a real network.

Skills Demonstrated

• Cisco IOS CLI
• IPv4 Addressing and Subnetting
• OSPF Routing
• DHCP Configuration
• SSH Remote Management
• NAT/PAT
• EtherChannel 
• Network Troubleshooting
• Network Verification
