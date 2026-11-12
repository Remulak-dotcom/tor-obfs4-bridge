Project Architecture

Overview
This project uses a remotely hosted Debian 13 server to operate a Tor obfs4 bridge.
The bridge acts as an alternative entry point to the Tor network. It allows users who may have difficulty connecting to Tor directly to establish a connection through an obfs4 transport.

How It Works
1. A user opens Tor Browser and configures an obfs4 bridge connection.
2. Tor Browser connects to the bridge server.
3. The obfs4 transport helps disguise recognizable Tor traffic.
4. The bridge forwards the connection into the Tor network.
5. Tor routes the user's traffic through its network.

Infrastructure Components
-VPS: Hosts the bridge remotely.
-Debian 13: Operating system running on the server.
-Tor: Provides the underlying network infrastructure.
-obfs4proxy: Provides the obfs4 transport.
-OpenSSH: Allows secure remote administration.
-nftables: Controls incoming and outgoing network traffic.

Network Services
The deployment uses separate network ports for bridge traffic and remote administration. 
Sensitive connection details, server addresses, and bridge credentials are intentionally excluded from this documentation.

Security Considerations
The server is configured with restricted network access, SSH key-based authentication, and firewall rules.
Administrative access is separated from the public bridge service to reduce unnecessary exposure.

Project Status
The bridge was successfully deployed and tested using Tor Browser.
