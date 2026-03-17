---
layout: post
title: HTTP vs HTTPS
---

HTTPS can transform data using a more secure way(using SSL/TLS). There are two aspects of it: Encryption and Certificate.
The servers which want to use HTTPS must get one CA certificate.
During the communication with clients, servers should send the certificate at the same time. Clients will check the certificate to ensure its security.

## Encryption
There are two types of encryption methods used in HTTPS.
### Asymmetric Encryption
Asymmetric encryption use a publich key and a privete key. The servers using HTTPS pack the public key in certificate and send it to clients. Clients will use this public key to make sure the identity.
### Symmetric Encryption
Symmetric Encryption is used after the first esteblishment of connection. It will make the transformation faster and take large amount of data.
