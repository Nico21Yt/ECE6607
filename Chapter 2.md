          1---
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
- Some apps (e.g., Internet telephony, inter`active games) require low delay to be “effective” 

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

### 2.2.4 cookies
- Many major Web sites use cookies 
- Four components
- What cookies can bring?(4 aspects)
- Cookies and privacy

## 2.3 Electronic Mail
- Three major components: user agent, mail server, SMTP

### 2.3.1 SMTP
- Three phases in message transfer: Handshaking (greeting), Transfer of messages, Closure
- Command/response interaction: ASCII text/ status code and phrase
- All Messages must be in 7-bit ASCII

### 2.3.2 Comparison with HTTP
- HTTP pull vs SMTP push
- SMTP need all 7-bit ASCLL
- HTTP encapulate each object in the responce msg while SMTP put all objects in one msg

### 2.3.3 Mail Message format

### 2.3.4 Mail Access protocol

## 2.4 DNS: DOMAIN NAME SYSTEM

### 2.4.1  What service DNS provides?
####  DNS provides translation between host name and IP address
#### What DNS is ?
- A distributed database implemented by a hierarchy of DNS servers.
- An application layer protocol that allows hosts to query the distributed database.
#### Services Provided
- host aliasing
- mail server aliasing
- Load distribution: DNS servers respond with a set of IP addresses and rotate the order in each answer, as clients tend to send HTTP request messages to the server whose IP address appears first.

### 2.4.2 Overview of DNS Working Mechanism
#### Simple design: centralized design, one DNS server for all
- possible issue: a single point of failure, traffic volume, distant centralized database and maintenance

#### Design: Distributed, hierachical database
#### Server types: 
- Root DNS server: offer the IP address of all TLD servers
- Top level domain(TLD) DNS servers for each top level domain(e.g., .com, .org, .edu)
- Authoritative DNS servers: Every organization with publicly accessible hosts on the Internet must provide publicly accessible DNS records.
- Local DNS servers: Every ISP has a local DNS server.

#### DNS caching

#### DNS Records and Messages
- Resource Record (RR) is a 4-tuple containing the following fields: (Name, Value, Type, TTL).
- If Type=A, then Name is the hostname, and Value is the IP address associated with that hostname.
- If Type=NS, then Name is a domain(like foo.com), and Value is the hostname of the authoritative DNS server within that domain.
- If Type=CNAME, then Name is a host alias, and Value is its canonical hostname.
- If Type=MX, then Name is a mail server alias, and Value is its canonical hostname.

## 2.5 P2P File Distribution

## 2.6 Video Streaming and Content Distribution Networks
### 2.6.1 Internet Video
- Compression algorithms can compress a video to any bitrate. The higher the bitrate, the better the image quality.
- Users watching Internet videos can choose different bitrate versions according to their currently available bandwidth.

### 2.6.2 HTTP Streaming and DASH
- Dynamic Adaptive Streaming over HTTP (DASH) encodes a video into several different versions, each with a different bitrate corresponding to different quality levels.
- An HTTP server using DASH has a manifest file that provides a URL and its bitrate for each video version, allowing customers to switch freely.

### 2.6.3 Content Delivery Networks (CDN)
- CDN manages servers located in multiple geographical locations, stores copies of data on its servers, and tries to direct each user request to a CDN location where the user experience is best.

### Server Placement Principles
- Deep penetration: Deploying server clusters throughout global access ISPs to penetrate into the ISPs' access networks.
- Inviting as a guest: Building large clusters at a few key locations to invite ISPs as guests. CDNs often place their clusters at Internet Exchange Points (IXPs).

### CDN Operations
- CDNs use the web site's DNS servers to intercept and redirect requests.
### Cluster Selection Strategies
#### Selecting the geographically closest cluster to the customer has drawbacks:
- The customer's local DNS server (LDNS) may be located far from the customer.
- This simple strategy ignores that delay and available bandwidth can vary with the Internet path.
#### Deciding the best cluster for the customer based on current traffic conditions:
- The CDN performs periodic real-time measurements of the delay and packet loss performance between its clusters and customers. For example, a CDN might have each of its clusters periodically send probe packets to all LDNS around the world.
- Drawback: Many LDNS are configured not to respond to these probes.





