## Transport Layer Functionality
The transport layer, or layer 4 of the OSI model, controls network traffic between hosts and end systems to guarantee full data flows.

| Function                                  | Description                                                                                                                                       |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Multiplexing and Demultiplexing           | Based on destination port number the receiving hosts choose correct application for which data is destined to                                     |
| Error Recovery                            | Process of acknowledgment of data based on it is sequence and it is ACK  header fields                                                            |
| Flow Control & Windowing                  | Sliding window size and making it flexible based on agreement between the two end devices dynamically                                             |
| Connection Esatblishiment and termination | Initializing the port numbers and ACK fields                                                                                                      |
| QOS(Quality of service)                   | The priority of services as the video takes higher priority than text for example so it optimize performance and the stability of user connection |
|                                           |                                                                                                                                                   |
![[functions_of_transport_layer.webp]]
**End to end communication  based on TCP/IP model**
![[functions_of_transport_layer_1.webp]]
**Multiplexing and Demultiplexing of the processes**
![[functions_of_transport_layer_4.webp]]
**Three way handshake connection establishment presentation**
![[functions_of_transport_layer_5.webp]]
**Connection Terminition Representation**
![[functions_of_transport_layer_6.webp]]
## Socket ##

- **Well Known (System Ports) Ports:** Numbers from 0 to 1023, assigned by IANA(Internet Assigned numbers authority), with a stricter review process to assign new ports than user ports.
- **User (Registered) Ports:** Numbers from 1024 to 49151, assigned by IANA with a less strict process to assign new ports compared to well-known ports.
- **Ephemeral (Dynamic, Private) Ports:** Numbers from 49152 to 65535, not assigned and intended to be dynamically allocated and used temporarily for a client application while the app is running.
## TCP(Transmission control protocol)
[TCP (Transmission Control Protocol)](https://www.geeksforgeeks.org/computer-networks/what-is-transmission-control-protocol-tcp/) is one of the main protocols of the Internet protocol suite. It lies between the Application and Network Layers which are used in providing reliable delivery services. It is a connection-oriented protocol for communications that helps in the exchange of messages between different devices over a network. The Internet Protocol (IP), which establishes the technique for sending data packets between computers, works with TCP.
![[TCP-1.png]]
**Advantages and Disadvantages of TCP**

| Advantages                                                                 | Disadvantages                                                |
| -------------------------------------------------------------------------- | ------------------------------------------------------------ |
| It is reliable for maintaining the connection between Sender and Receiver. | It is responsible for sending data in a particular sequence. |
| It is responsible for sending data in a particular sequence.               | It does not have a multicast or broadcast category.          |
## UDP(User Datagram Protocol)
[User Datagram Protocol (UDP)](https://www.geeksforgeeks.org/computer-networks/user-datagram-protocol-udp/) is a Transport Layer protocol. UDP is a part of the Internet Protocol suite, referred to as the UDP/IP suite. Unlike TCP, it is an unreliable and connectionless protocol. So, there is no need to establish a connection before data transfer. The UDP helps to establish low-latency and loss-tolerating connections establish over the network. The UDP enables process-to-process communication.
![[TCP-2.png]]
**Advantages and Disadvantages of UDP**

| Advantages                                                             | Disadvantages                                                                               |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Broadcast and multicast are avaliable in the UDP protocol.             | We can not have any way to acknowledge the successful transfer of data So,It is unreliable. |
| UDP has live and real-time data So it is usually used in live streams. | In case of a Collision, UDP packets are dropped by Routers in comparison to TCP.            |
