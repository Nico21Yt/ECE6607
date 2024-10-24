---
title: Chapter 4, Network Layer Overview
markmap:
  colorFreezeLevel: 2
---

## 4.1 Network Layer Overview
- Dataplane: Forwarding
- ControlPlane: Routing decision
- Traditional approach: Routers communicate with each other to calculate the values for the forwarding table.
- SDN(Software Defined Networking) approach: A remote controller is used to calculate and distribute the forwarding table.
- Guaranteed delivery, possibly with an upper bound on delay and services for ordered packet delivery.
- Network service model ensures minimum bandwidth and security.
- Internet network layer service model: Best-effort service

## 4.2 How routers work

###
- Line termination: Physical layer processing
- input ports: Data link processing(protocols, unencapsulating)
- Lookkup, forwarding, and queuing
- Switching fabrit: Connects input ports to output ports
- Router architecture: Queue management(buffer management).
-  Output ports: Data link processing(protocols, encapsulating)
- Line termination
- Routing processor:
- Lookup

### 4.2.1 Input Port Processing and Destination-Based Forwarding

