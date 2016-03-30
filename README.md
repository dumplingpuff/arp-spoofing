# ARP Spoofing

ARP spoofing is an attack when an attacker sends out fake ARP messages over a
local area network(LAN) that allows the attacker to link it's MAC address with
the IP address of another computer. This means the attacker will be allowed to
receive any data or traffic sent to that intended IP address.  From this point
if the attacker is malicious he or she can read, modify, or stop the data flow
from the router and the intended victim computer.  Such attacks only happens on
local networks. This is because ARP protocols are not authenticated.

![Isn't that Middle Man?](http://imgur.com/BKig86m.jpg)

## How it works (ARP Process on LAN)

ARP is the address resolution protocols that are used by machines on a Local
Area Network(LAN) to communicate with each other. On local area network or LAN
computers are located by their MAC address through the use of ARP messages.
On a local network on MAC address can transmit data not IP addresses, IP address
is used to communicate outside of the network. Everything on the local network
has a IP address and MAC address even routers, this is important.

So the wireless routers are the default gateway for computers to reach the
outside world. When a default gateway wants a particular IP address of a
computer it would send out ARP messages to all computers waiting for a reply.
The computer of the right MAC address would receive and then save the addresses
of the router.  Then it would send an ARP back to the router which saves the
computer's IP and MAC address on a cache. The router is dumb and typically
forgets this information so it is constantly asking for these addresses.

When this happens ARP spoofers would try to send a fake message tricking both
parties into the spoofer's MAC address is attached to the router's IP address
and vice versa.

![Stranger Danger](http://i.imgur.com/jYZQ3aO.jpg)

## Defenses Against ARP Spoofing

Packet filtering: Packet filters inspect packets being transmitted across a
network. They detect ARP spoofing by looking at packets with conflicting source
address information
(packets from outside the network that show source addresses from
inside the network and vice-versa).

Avoid trust relationships: Trust relationships uses IP address for
authentication.

ARP Spoofing Detection Software: Program inspects data before it is
transmitted, if it is spoofed the data will be blocked

Use cryptographic network protocols:
Transport Layer Security (TLS), Secure Shell (SSH), HTTP Secure (HTTPS) will
encrypt data before it is sent out and authenticate data when it comes in.

## Tools for ARP Spoofing

PacketCreator
Ettercap
Dsniff
Cain e Abel

## More Info MAC Addresses

MAC addresses are called the physcial address, this is because these addresses
are assigned by the manufacturer of a network interface controller



A media access control address (MAC address), also called physical address, is a unique identifier assigned to network interfaces for communications on the physical network segment. MAC addresses are used as a network address for most IEEE 802 network technologies, including Ethernet and WiFi. Logically, MAC addresses are used in the media access control protocol sublayer of the OSI reference model.

MAC addresses are most often assigned by the manufacturer of a network interface controller (NIC) and are stored in its hardware, such as the card's read-only memory or some other firmware mechanism. If assigned by the manufacturer, a MAC address usually encodes the manufacturer's registered identification number and may be referred to as the burned-in address (BIA). It may also be known as an Ethernet hardware address (EHA), hardware address or physical address. This can be contrasted to a programmed address, where the host device issues commands to the NIC to use an arbitrary address.

A network node may have multiple NICs and each NIC must have a unique MAC address.
