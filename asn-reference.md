
# ASN Reference for Security Architects

## What is an ASN?
An Autonomous System Number uniquely identifies a network or group of IP prefixes under a single administrative entity, particularly relevant for BGP.

## Types
- Public ASN: Assigned by RIRs (e.g., 7224 for AWS)
- Private ASN: 64512–65534 (16-bit), 4200000000–4294967294 (32-bit)

## Why It Matters
- Prevent route leaks
- Secure multi-cloud peering
- Required for BGP routing

## Threat: ASN Hijacking
Attackers can announce IP prefixes using forged ASNs. Prevent with:
- Prefix filtering
- RPKI
- BGP session authentication (MD5)
