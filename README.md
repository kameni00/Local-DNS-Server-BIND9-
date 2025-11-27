# Local-DNS-Server-BIND9-
A local DNS server setup using Bind9 with custom zones, caching, controlled recursion, and SOA configuration.

Project summary

A compact, professional demonstration of a local authoritative DNS server built with BIND9 on Ubuntu (VirtualBox VM). The repository contains configuration files, test commands and screenshots that prove the server is authoritative for project.local, serves A/CNAME/MX/NS/SOA records, performs caching, and recursion when internet connectivity is present.

Overview

This project documents the end-to-end setup and verification of a local DNS service using BIND9. It is suitable for inclusion in a CV or GitHub portfolio and is intentionally concise while remaining technical and reproducible.

Contents of this repository

dns-project/
├── README.md 
├── zones/
│ └── db.project.local # Zone file (authoritative records)
└── screenshots/
  ├── soa.png
  ├── ns.png
  ├── a_records.png
  ├── cname.png
  ├── mx.png
  ├── recursion.png
  └── ping.png

1. Requirements

-Ubuntu (tested on Ubuntu 22.04 / 24.04 LTS) running in VirtualBox

-BIND9 (bind9, bind9utils, bind9-doc)

-Sudo/root privileges

-Optional: internet access (for recursion tests)
