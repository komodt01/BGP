
# Multi-Cloud BGP + ASN Security Architecture

This repository documents a real-world hybrid cloud architecture with BGP routing and Autonomous System Numbers (ASN) as relevant to security architects.

## Contents
- Cheat sheet for routing protocols
- AWS Direct Connect example using BGP
- Multi-cloud setup (AWS, Azure, On-Prem) with ASNs
- Security checklists
- Architecture diagram

---

## 🔐 Security Architect Routing Cheat Sheet

| Protocol | Type | Who Uses It | Summary | Security Notes |
|----------|------|-------------|---------|----------------|
| RIP | IGP | Legacy | Max 15 hops | No encryption |
| OSPF | IGP | Enterprises | Fast, scalable | Use MD5 auth |
| IGRP | IGP | Cisco-only | Obsolete | No modern security |
| EIGRP | IGP | Cisco-only | Fast, supports VLSM | Use auth |
| BGP | EGP | ISPs/cloud | Internet routing using ASN | RPKI, MD5, filtering |

See `asn-reference.md` and `security-checklist.md` for more.

---

## 🛠 AWS Direct Connect BGP Example

ASN: 64512  
AWS ASN: 7224  
Route: 10.0.0.0/16 (advertised)  
See `bgp-config-examples/aws-directconnect-bgp.txt`

---

## 🌍 Multi-Cloud ASN + BGP Architecture

Transit Gateway ASN: 64513  
Azure ASN: 12076  
On-Prem ASN: 64512  

Refer to `architecture-diagram.png` and `bgp-config-examples/multicloud-bgp-summary.txt`

---

## ✅ Security Focus Areas
- BGP MD5 auth
- Prefix filtering
- ASN hijack prevention
- Route segmentation
- Logging + monitoring

