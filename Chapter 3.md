---
title: Chapter 3, Transport layer
markmap:
  colorFreezeLevel: 2
---

# 3.1 Introduction and Transport-Layer Services
## 3.1.1 Relationship between the Transport Layer and Network Layer
- The transport layer provides logical communication between processes on different hosts, while the network layer provides logical communication between hosts.
- Transport layer protocols operate only in end systems, not in network devices(routers)
- More than one transport protocol available to apps(e.g.TCP and UDP)

## 3.1.2 Overview of the Transport Layer in the Internet
- PDU: Segment, while PDU in Network layer is Datagram
- IP service model: a best-effort delivery service

# 3.2 Multiplexing and Demultiplexing
- Multiplexing: The source host collects data blocks from different sockets, encapsulates them into segments, and then delivers the segments to the network layer.

- Demultiplexing: Delivering the data from the transport layer segments to the correct sockets.

- Essential fields in segments: source port number and destination port number.

# 3.3 Connectionless Transport: UDP
## 3.1 
- Reasons for using UDP include more refined control over what the application layer can manage.
- UDP can immediately package and send data, whereas TCP's congestion control mechanisms might restrain the sender.
- Real-time applications prefer not to delay sending excessively and can tolerate some data loss, making UDP more suitable for such applications.
- UDP does not maintain connection state, which supports more active users with less overhead.
- Header overhead is smaller for UDP (8 bytes) compared to TCP (20 bytes).

# 3.4 Principles of Reliable Data Transfer
# 3.5 Connection-Oriented Transport: TCP
# 3.6 Principles of Congestion Control
# 3.7 TCP Congestion Control
