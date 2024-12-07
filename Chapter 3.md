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
## 3.3.1 
- Reasons for using UDP include more refined control over what the application layer can manage.
- UDP can immediately package and send data, whereas TCP's congestion control mechanisms might restrain the sender.
- Real-time applications prefer not to delay sending excessively and can tolerate some data loss, making UDP more suitable for such applications.
- UDP does not maintain connection state, which supports more active users with less overhead.
- Header overhead is smaller for UDP (8 bytes) compared to TCP (20 bytes).

##
# 3.4 Principles of Reliable Data Transfer
## 3.4.1 Construction of reliable data transfer protocols(RDT1.0, RDT2.O...)
## 3.4.2 Automatic Repeat reQuest (ARQ) protocols and error recovery mechanisms.

# 3.5 Connection-Oriented Transport: TCP
- TCP connections are full-duplex and point-to-point.
- The structure of TCP segments, including sequence numbers and acknowledgments.
- Flow control to prevent receiver buffer overflow.
- Connection management with the three-way handshake for establishing a connection and four-way handshake for closing a connection.


# 3.6 Principles of Congestion Control
- Causes and costs of network congestion.(2 cases)
- End-to-end congestion control methods used by TCP due to the lack of feedback from the network layer about network congestion.

# 3.7 TCP Congestion Control
- Slow start, congestion avoidance, and fast recovery algorithms.
- Additive increase, multiplicative decrease (AIMD) congestion control.
- Calculating TCP throughput using a simplified model.
- Fairness in congestion control across multiple TCP connections sharing the same bottleneck link.
- Explicit Congestion Notification (ECN) for providing feedback about network congestion directly from the network layer.

