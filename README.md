# Local DNS Server (BIND9) -- Project Documentation

This project showcases a professionally configured **local DNS server
using BIND9**, designed for portfolio demonstration and practical system
administration experience.\


------------------------------------------------------------------------

## 📌 Project Overview

A fully functional **local DNS server** built with BIND9 on Ubuntu (VirtualBox),
featuring:

-   Custom forward and reverse lookup zones
-   SOA, NS, A, MX, CNAME records
-   Controlled recursion
-   DNS caching
-   DNS query testing and validation using `dig`, `nslookup`, and logs

------------------------------------------------------------------------

## 📂 Directory Structure 

    /project-root
    ├── README.md
    └── images/
        ├── setup-01.png
        ├── setup-02.png
        ├── zone-forward.png
        ├── zone-reverse.png
        ├── named-conf-local.png
        ├── bind-service.png
        ├── dig-test-forward.png
        ├── dig-test-reverse.png
        ├── recursion-test.png
        ├── caching-test.png
        └── logs-query.png



------------------------------------------------------------------------

# 📸 Screenshots 

## 1. System Preparation

-   Installing required packages\
    `sudo apt install bind9 bind9utils bind9-doc -y`\
    ![Package installation](images/install.png)

-   Verifying service status\
    ![Service status](images/bind-service.png)

------------------------------------------------------------------------

## 2. Configuration Files

### **named.conf.local**

-   Forward and reverse zone declarations\
    ![named.conf.local](images/named-conf-local.png)

### **Forward Zone File**

-   Example forward zone structure\
    ![Forward zone file](images/zone-forward.png)

### **Reverse Zone File**

-   PTR records and reverse mapping\
    ![Reverse zone file](images/zone-reverse.png)

------------------------------------------------------------------------

## 3. Testing & Validation

### **Forward Lookup Test**

`dig yourdomain.local`\
![Forward lookup test](images/dig-test-forward.png)

### **Reverse Lookup Test**

`dig -x 192.168.x.x`\
![Reverse lookup test](images/dig-test-reverse.png)

### **Recursion Testing**

Shows controlled recursion behavior when querying external domains.\
![Recursion test](images/recursion-test.png)

### **Caching Test**

Demonstrates reduced response time on repeated queries.\
![Caching test](images/caching-test.png)

### **Query Logging**

DNS query logs from `/var/log/syslog`\
![DNS logs](images/logs-query.png)

------------------------------------------------------------------------

# 🧩 Features Implemented

### ✔️ **Local Zone Hosting**

Custom domain + reverse zone mapping.

### ✔️ **Controlled Recursion**

Only allowed for LAN devices; blocked for external networks.

### ✔️ **DNS Caching**

Speeds up repeated queries and reduces load.

### ✔️ **Service Management**

Start/stop/status controls using systemd.

------------------------------------------------------------------------

# 🛠️ Technologies Used

-   Ubuntu Linux\
-   BIND9 / Bind9utils\
-   dig / nslookup\
-   systemd\
-   Bash

------------------------------------------------------------------------

# 📚 How to Use

1.  Clone the repository\
2.  Replace screenshot placeholders under `/images`\
3.  Use this README as your GitHub project presentation

------------------------------------------------------------------------

# 🏁 Final Notes

This README is structured for professional presentation on GitHub and CV
portfolios.\
All screenshot placeholders are clearly labeled --- just drop your
images into the `images/` folder and match the file names.
