# 🛡️ SafeLine WAF Home Lab – Web Application Security Lab

## Overview

This project demonstrates the deployment and configuration of a complete Web Application Firewall (WAF) Home Lab using SafeLine WAF, DVWA (Damn Vulnerable Web Application), Ubuntu Server, and Kali Linux.

The objective was to understand how modern WAF solutions protect vulnerable web applications against common web attacks while gaining hands-on experience with web application security, reverse proxying, SSL/TLS, authentication gateways, and attack monitoring.

This lab was inspired by Royden Rebello (The Social Dork) and his SafeLine WAF Home Lab guide.

---

## Lab Architecture

Kali Linux (Attacker Machine)

↓

SafeLine WAF (Reverse Proxy + Protection Layer)

↓

DVWA Web Server (Ubuntu)

---

## Technologies Used

* SafeLine WAF
* DVWA (Damn Vulnerable Web Application)
* Ubuntu Server
* Kali Linux
* Apache2
* PHP
* MySQL/MariaDB
* OpenSSL
* VMware Workstation
* Linux Networking
* HTTPS/TLS

---

## Project Objectives

* Deploy a vulnerable web application
* Configure a Web Application Firewall
* Protect DVWA using SafeLine WAF
* Implement HTTPS communication
* Configure custom domain resolution
* Test WAF protection capabilities
* Explore authentication and flood protection features

---

## Environment Setup

### Ubuntu Server

Configured as:

* Apache Web Server
* PHP Runtime
* MySQL/MariaDB Database Server
* DVWA Host

### Kali Linux

Configured as:

* Attacker Machine
* Security Testing Workstation

### Networking

* Bridged Networking
* Custom Domain Resolution
* HTTPS Access through SafeLine WAF

---

## What I Implemented

### 1. LAMP Stack Installation

Installed and configured:

* Apache2
* PHP
* MySQL/MariaDB

### 2. DVWA Deployment

* Downloaded DVWA
* Configured file permissions
* Created database
* Configured database users
* Reset and initialized DVWA database

### 3. Apache Reconfiguration

* Changed listening port from 80 to 8080
* Configured virtual hosts

### 4. DNS Resolution

Configured local DNS/Hosts file entries:

webserver.devil666

This allowed domain-based access instead of raw IP addresses.

### 5. SSL/TLS Setup

Generated and configured:

* Self-signed SSL Certificate
* HTTPS connectivity

### 6. SafeLine WAF Installation

Installed SafeLine WAF and configured:

* Reverse Proxy
* HTTPS Frontend
* Backend Application Mapping
* Domain Matching

### 7. Application Protection

Protected:

DVWA → SafeLine WAF → HTTPS Access

### 8. Authentication Gateway

Configured SafeLine Authentication Module:

* Username Authentication
* Login Validation
* Access Control

### 9. HTTP Flood Protection

Configured:

* Request Rate Limiting
* Temporary Blocking
* Flood Detection

Successfully observed blocked requests and rate-limiting events.

---

## Major Challenges Faced

### MySQL Authentication Issues

Issue:

Access denied for user 'dvwa'@'localhost'

Resolution:

* Created database user
* Reset credentials
* Updated DVWA configuration

### Missing DVWA Configuration

Issue:

config.inc.php not found

Resolution:

Created:

config/config.inc.php

from:

config/config.inc.php.dist

### Apache Path Issues

Issue:

404 Not Found

Resolution:

Moved DVWA into Apache Document Root

### SafeLine Domain Mismatch

Issue:

Website Not Found

The Domain Name You Visited Does not Match The Server

Resolution:

Corrected Host Header and Domain Mapping configuration.

### SafeLine Authentication

Successfully configured and validated:

* Authentication Gateway
* Login Attempts
* Successful and Failed Login Tracking

---

## Skills Strengthened

### Web Security

* Web Application Firewalls
* OWASP Concepts
* Authentication Security
* Reverse Proxy Security

### Linux Administration

* Apache Configuration
* Service Management
* File Permissions
* Package Management

### Networking

* DNS Resolution
* Host Mapping
* Bridged Networking
* HTTPS/TLS

### Database Administration

* MySQL User Management
* Database Initialization
* Authentication Troubleshooting

### Troubleshooting

* Apache Errors
* PHP Errors
* Database Errors
* WAF Misconfigurations

---

## New Concepts Learned

* WAF Architecture
* Reverse Proxy Security
* Host Header Validation
* TLS Certificate Deployment
* Rate Limiting
* HTTP Flood Mitigation
* Authentication Gateways
* Web Application Protection Workflow

---

## SafeLine WAF Advantages

### Pros

✅ Easy Deployment

✅ User-Friendly Dashboard

✅ HTTPS Support

✅ Authentication Gateway

✅ HTTP Flood Protection

✅ Reverse Proxy Architecture

✅ SQL Injection Detection

✅ Real-Time Monitoring

✅ Request Analytics

✅ IP Blocking

✅ Application-Level Security

---

## SafeLine WAF Limitations

### Cons

❌ Requires Proper DNS Configuration

❌ False Positives Possible

❌ Self-Signed Certificates Create Browser Warnings

❌ Learning Curve for Initial Setup

❌ Advanced Features Require Premium License

❌ Does Not Replace Secure Coding Practices

---

## Time Invested

Approximate Project Duration:

* Initial Setup: 2–3 Hours
* Troubleshooting: 3–4 Hours
* WAF Configuration: 1–2 Hours
* Testing and Validation: 1 Hour

Total Time Invested:

~7–10 Hours

---

## Key Takeaway

This project provided hands-on experience in deploying, configuring, and defending a vulnerable web application using a modern Web Application Firewall.

Beyond installation, the most valuable learning came from troubleshooting real-world issues involving Apache, MySQL, DNS, HTTPS, reverse proxies, and WAF policies.

The lab strengthened practical skills in both offensive and defensive security while providing deeper insight into how modern web application protection works.

---

## Credits

Guide and Inspiration:

Royden Rebello (The Social Dork)

Special thanks for providing the SafeLine WAF Home Lab guide and educational content that helped build this project.

