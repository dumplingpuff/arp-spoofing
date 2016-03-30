# ARP Spoofing

ARP spoofing is an attack when an attacker sends out fake ARP messages over a
local area network(LAN) that allows the attacker to link it's MAC address with
the IP address of another computer. This means the attacker will be allowed to
receive any data or traffic sent to that intended IP address.  From this point
if the attacker is malicious he or she can read, modify, or stop the data flow
from the router and the intended victim computer.  Such attacks only happens on
local networks. This is because ARP protocols are not authenticated.

![Isn't that Middle Man?](http://imgur.com/BKig86m.jpg)

![Stranger Danger](http://i.imgur.com/jYZQ3aO.jpg)

## How it works (ARP Process on LAN)

![YO MAC ADDRESS](http://i.imgur.com/yaWVKOV.png)

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

[ARP Cache](http://i.imgur.com/VGaop6C.jpg)

When this happens ARP spoofers would try to send a fake message tricking both
parties into the spoofer's MAC address is attached to the router's IP address
and vice versa.

[Creepy Computers](http://i.imgur.com/GI6i0qO.png)

## Signs of Spoofing

Multiple IP addresses associated with a single MAC address,
although there are legitimate uses of such a configuration.

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

## Getting Data from HTTPS not HTTP

Like mentioned above cryptograhic network protocols like HTTPS can help with
ARP spoofing. When the data gets sent back it is encrypted so the contents
of the packet can't be seen. In HTTP it is left bare so you can see the
password, username, and website the browser is accessing.

## Protecting Yourself

Arpwatch
Antidote: Linux daemon, monitors mappings, unusually large number of ARP packets
DefendARP: A host-based ARP table monitoring and defense tool designed for
use when connecting to public wifi. DefendARP detects ARP poisoning attacks,
corrects the poisoned entry, and identifies the MAC and IP address of the
attacker.

## Tools for ARP Spoofing

PacketCreator
Ettercap
Dsniff
Cain e Abel

## More Info MAC Addresses

MAC addresses are called the physcial address, this is because these addresses
are assigned by the manufacturer of a network interface controller

## Example

[cisco](http://www.cisco.com/c/en/us/products/collateral/switches/catalyst-6500-series-switches/white_paper_c11_603839.html)

[ettercap diagram](http://openmaniak.com/ettercap.php#diagram)

[WireShark shows red](http://openmaniak.com/ettercap_arp.php)
