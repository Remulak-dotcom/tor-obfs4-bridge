Deployment Documentation

Overview
This document describes the deployment of a self-hosted Tor obfs4 bridge on a Debian 13 virtual private server.
The deployment involved preparing the Linux environment, configuring Tor, installing and configuring the obfs4 transport, securing remote administration, and verifying that the bridge was operational.

Server Preparation

A virtual private server was provisioned with the following environment:
-Debian 13 (64-bit)
-AMD64 architecture
-2 CPU cores
-1 GB RAM
-20 GB SSD storage

The server was accessed remotely using OpenSSH.

Remote Access Configuration
SSH was configured to provide secure administrative access.
An Ed25519 SSH key pair was generated for key-based authentication. A dedicated administrative account was used to manage the server.

Tor Installation and Configuration
Tor was installed and configured on the Debian server.

The configuration included:
-Tor service configuration.
-Bridge operation.
-Network port configuration.
-Service startup and verification.

The Tor service was confirmed operational.

obfs4 Transport Configuration

The obfs4 pluggable transport was installed and configured using obfs4proxy.
The transport provides an alternative way for Tor users to connect to the bridge while making recognizable Tor traffic more difficult to identify.
The obfs4proxy process was verified to be running and listening on its configured port.

Firewall Configuration

nftables was configured to control network access to the VPS.
Firewall rules were established to permit required network services while restricting unnecessary inbound traffic.

Deployment Verification
After configuration, the deployment was verified through:

-Tor service status checks.
-obfs4proxy process verification.
-Listening-port inspection.
-External reachability testing.
-Successful connection through Tor Browser.

The bridge successfully reached operational status.

Deployment Outcome
The VPS successfully hosts a functioning Tor obfs4 bridge.
The deployment provided practical experience with Linux administration, remote server management, network configuration, firewall security, and privacy infrastructure.
