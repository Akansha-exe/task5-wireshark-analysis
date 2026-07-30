Network Traffic Analysis Report

1. Capture Overview

Duration: ~1 minute
Interface used: Wi-Fi / Ethernet
Activity generated: browsed google.com, wikipedia.org; ran ping google.com

2. Protocols Identified

DNS (Domain Name System)

Purpose: resolves domain names (e.g., google.com) to IP addresses
Sample packet: Query for google.com → Response with IP 142.250.x.x
Port used: 53

TCP (Transmission Control Protocol)

Purpose: reliable connection setup between client and server
Sample: SYN → SYN-ACK → ACK handshake seen before HTTPS traffic to [IP]

TLS/HTTPS

Purpose: encrypted web traffic
Sample: Client Hello to server IP on port 443, followed by encrypted application data
Note: most modern browsing traffic showed up as TLS, not plain HTTP, since almost all sites now use HTTPS

ICMP (Internet Control Message Protocol)

Purpose: used by ping to test reachability
Sample: Echo Request to google.com, Echo Reply received, showing round-trip time

3. Observations

Majority of traffic was encrypted (TLS), reflecting modern web security practices
DNS queries preceded almost every new connection, confirming its role as the "phonebook" of the internet
ICMP traffic was minimal and only appeared due to manual ping testing

4. Conclusion

Gained hands-on experience identifying protocols in real traffic and understanding how a simple web request involves multiple layers (DNS → TCP → TLS/HTTP)
