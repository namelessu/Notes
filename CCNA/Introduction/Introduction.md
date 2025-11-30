## Network Definiton
- It is a collection of devices connected together to provide a certain service to the user.
- Services includes Data sharing,Resource sharing, Modern technology (VOIP, video conference, clouding, IOT, BYOD, etc)
## Network components
- End Devices: PC's , Printers, Smarphones, etc.
- Network Devices: Routers, Hub, Switches, Repeaters, Access points, etc.
- Connection media: wireless media and wired media.
## Network topologies
- Bus Topology: It is a type of connection where network end devices are connected to a coaxial cable with a connector called T-connector, Such a topology had many problems such as data loop which was fixed by adding terminator resistances at both ends of the wire, Another problem is that the data must be sent to all devices and dropped by each device except the device that needs it, Another major problem was the collision of data lets say that there are two devices sending to a certain device data at the same time collision happen which was fixed by software called CSMA/CD (Collision sense multiple access over collision detection).

![[Bus Topology.webp]]
- Star topology: In this topology the end devices are connected to a network device connector such as hub or switch. In case of hub the hub floods data to all devices except the ingress data port the incoming data port which is bad. Also the collision can happen when two end devices send to a certain device at the same time. In case of switch the first frame is flood to all devices except ingress port and the device fills the mac address table with the ingress port and it is mac and this happen till the mac address table is filled. So only the first frame is flood.

![[The-star-network-topology.webp]]

- Ring topology: Such as FDDI and token ring.

![[ring-topology4.webp]]
- Mesh topology: is a redundant topology.

![[Mesh Topology.webp]]