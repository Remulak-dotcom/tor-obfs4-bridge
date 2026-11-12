Testing and Verification

Overview
The Tor obfs4 bridge was tested to verify that the deployment was operational and that clients could successfully connect through the bridge.

Service Verification
The following checks were performed on the Debian 13 VPS:

-Confirmed that the tor@default service was active.
-Verified that Tor successfully completed its bootstrap process.
-Confirmed that obfs4proxy was running.
-Verified that obfs4proxy was listening on TCP port 4433.
-Verified that the Tor ORPort on TCP port 9002 was externally reachable.

Client Connectivity Testing
The bridge was tested using Tor Browser with a manually configured obfs4 bridge connection.
Successful connectivity was confirmed using the Tor Project's connection verification page.

Backup Integrity Testing
An encrypted backup was transferred to a local ThinkPad running Trisquel Linux.
A SHA-256 checksum comparison confirmed that the transferred backup matched the original.

Results
The deployment successfully demonstrated:

-Tor service operation.
-obfs4 transport operation.
-External ORPort reachability.
-Successful Tor Browser connectivity.
-Encrypted backup integrity verification.

Evidence
Supporting screenshots are available in the screenshots/ directory.
