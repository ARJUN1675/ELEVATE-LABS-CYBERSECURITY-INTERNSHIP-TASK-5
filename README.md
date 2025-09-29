# ELEVATE-LABS-CYBERSECURITY-INTERNSHIP-TASK-5

**Task 5**  : Capture and Analyze Network Traffic Using Wireshark.

 **Objective**: Capture live network packets and identify basic protocols and traffic types.
 **Tools**: Wireshark (free).
 **Deliverables**:  A packet capture (.pcap) file and a short report of protocols identified.
 
 **Hints/Mini Guide:**
 1.Insta l Wireshark.
 2.Start capturing on your active network interface.
 3.Browse a website or ping a server to generate traffic.
 4.Stop capture after a minute.
 5.Filter captured packets by protocol (e.g., HTTP, DNS, TCP).
 6.Identify at least 3 different protocols in the capture.
 7.Export the capture as a .pcap file.
 8.Summarize your findings and packet details.

**Protocols Observed**
DNS – Domain resolution requests and responses.
TCP – Transport protocol for HTTP/HTTPS communication.
HTTP/HTTPS – Web browsing traffic (unencrypted/encrypted).
ICMP – Ping request/reply packets.

**Findings**
DNS lookups occur before HTTP traffic to resolve domain names.
TCP packets establish connections and transfer data.
HTTPS traffic is encrypted, so only handshake and metadata are visible.
ICMP packets confirm connectivity via ping.

---

#Advantages and disadvantages
## **1. DNS (Domain Name System)**
**Advantages:**
* Translates human-readable domain names (e.g., `google.com`) into IP addresses.
* Distributed and hierarchical system ensures scalability.
* Caching improves performance and reduces lookup time.
**Disadvantages:**
* DNS traffic is usually **unencrypted** (unless DNS-over-HTTPS/DoT is used), so attackers can sniff queries.
* Vulnerable to attacks like **DNS spoofing**, **cache poisoning**, or **DNS amplification (DDoS)**.
* Single point of failure if DNS servers are unavailable.

## **2. TCP (Transmission Control Protocol)**
**Advantages:**
* Reliable: ensures data is delivered correctly and in order.
* Connection-oriented: establishes a session before transmitting.
* Error detection and retransmission mechanisms.
**Disadvantages:**
* Higher overhead compared to UDP (due to acknowledgments, handshakes, retransmissions).
* Slower for real-time applications (e.g., video calls, gaming).
* Vulnerable to SYN flood attacks (DoS).

## **3. HTTP/HTTPS (Hypertext Transfer Protocol / Secure)**
**Advantages:**
* HTTP is simple and widely supported for web communication.
* HTTPS encrypts traffic, ensuring **confidentiality, integrity, and authentication**.
* Essential for secure e-commerce, banking, and sensitive data exchange.
**Disadvantages:**
* HTTP (unencrypted) is insecure: data can be intercepted or modified.
* HTTPS adds encryption overhead, making it slightly slower than HTTP.
* Requires digital certificates (PKI), which adds cost/management effort.

## **4. ICMP (Internet Control Message Protocol)**
**Advantages:**
* Useful for diagnostics (e.g., `ping`, `traceroute`).
* Lightweight protocol for error reporting and connectivity checks.
* Helps network admins detect routing or reachability issues.
**Disadvantages:**
* Provides limited information (not for data transfer).
* Can be abused in **ICMP flood (DoS)** or **Smurf attacks**.
* Sometimes blocked by firewalls, limiting troubleshooting ability.

---

**Deliverables**
Packet Capture File: network_traffic.pcapng
Report: This README document.
