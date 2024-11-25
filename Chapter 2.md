---
title: Chapter 2, Application Layer
markmap:
  colorFreezeLevel: 3
---

## 2.1 Application layer protocols
### 2.1.1 Application architectures

#### Client Server
- Server always on
- Client initiates communication
- Server with well-known (IP) address
- Clients don’t communicate directly with each other
- Typical apps: Web, FTP, Email,…
- What if the server not powerful enough? ➔DCs
#### Peer-to-peer (P2P)
- Direct communication between “peers” – intermittently connected hosts
- Self scalable
- Cost-effective
- Typical apps: File sharing (BitTorrent), Intenet tel & video…
#### Hybrid of client-server and P2P 
- Instant messaging: tracking IP addresses – server

### 2.1.2 Processes Communicating

#### Socket
- The (software) interface between the Process and
the Network

### 2.1.3 What transport service does an App need?
- Data loss / Reliable Data Transfer
- Bandwidth/Throughput
- Timing
- Some apps (e.g., Internet telephony, interactive games) require low delay to be “effective” 

### 2.1.4 Internet transport protocols services
#### TCP service: 
- Connection-oriented: Setup required between
client and server processes
- Reliable transport between sending and receiving
process
- Flow control: sender won’t overwhelm receiver 
- Congestion control: throttle sender when network
overloaded
- Does not provide: timing, minimum throughput
guarantees, security 
- Telephone

#### UDP service: 
- Unreliable data transfer between
- sending and receiving process
Does not provide: connection setup,
reliability, flow control, congestion
control, timing, throughput guarantee,
or security
- Postal service

### 2.1.5 Application-layer protocol
- How an application’s processes, running on different end systems, pass messages to each
other
- types: The types of messages exchanged, for example, request messages and response messages 
- syntax: The syntax of the various message types, such as the fields in the message and how the fields are
delineated
- semantics: The semantics of the fields, that is, the meaning of the information in the fields 
- rules: Rules for determining when and how a process sends messages and responds to messages

## 2.2 Web and HTTP
### 2.2.1 Overview of HTTP
- HTTP refers to HyperText Transfer Protocol
- URL: protocol + host name + pathname

### 2.2.2 non- persistent/ persistene connection
- Round-Trip Time, RTT
- 

### 2.2.3 HTTP format
- GET: retrieve a file (95% of requests)
- HEAD: just get meta-data (e.g., mod time)
- POST: submitting a form to a server
- PUT: store enclosed document as URI
- DELETE: removed named resource
- LINK/UNLINK: in 1.0, gone in 1.1
- TRACE: http “echo” for debugging (added in 1.1)
- CONNECT: used by proxies for tunneling (1.1)
- OPTIONS: request for server/proxy options (1.1)


