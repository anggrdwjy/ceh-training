## Module 3. Scanning Networks
#### A. Perform Host Discovery
* Task 1. Perform Host Discovery using NMAP
  * ARP Ping Scan
    ```
    nmap -sn -PR 172.23.74.125
    ```
  * UDP Ping Scan
    ```
    nmap -sn -PU 172.23.74.125
    ```
  * ICMP ECHO Ping Scan
    ```
    nmap -sn -PE 172.23.74.125
    ```
  * ICMP Timestamp Ping Scan
    ```
    nmap -sn - PP 172.23.74.125
    ```
  * ICMP Address Mask Ping Scan
    ```
    nmap -sn -PM 172.23.74.125
    ```
  * TCP SYN Ping Scan
    ```
    nmap -sn -PS 172.23.74.125
    ```
  * TCP ACK Ping Scan
    ```
    nmap -sn -PA 172.23.74.125
    ```
  * IP Protocols Ping Scan
    ```
    nmap -sn -PO 172.23.74.125
    ```

* Task 2. Perform Host Disvovery using Angry IP Scanner
  * Download Angry IP Scanner
  * Scanning IP Range 172.23.74.1 - 172.23.74.255
  * Hostname : Specific
  * IP : Netmask
  * Prefrences Scanning : Combined UDP+TCP
  * Prefrences Display : Alive hosts (responding to pings) only

#### B. Perform Port and Services Discovery
* Task 1. Perform Port and Service Discovery using MegaPing
  * Download Tools from : https://magnetsoft.com/producs-download
  * Install megaping_setup.exe
  * Running Tools MegaPing.exe

* Task 2. Perform Port and Service Discovery using NetScanTools Pro
  * Download Tools from : https://netscantools.com/ntbasicrequestform.html
  * Install netscantools_demo.exe

* Task 3. Perform Port Scanning using sx Tools
  * Detail Documents : https://github.com/v-byte-cpu/sx
  * ARP Scan
    ```
    sx arp 172.23.74.125/24
    sx arp 172.23.74.125/24 --json | tee arp.cache
    ```
  * TCP Scan
    ```
    cat arp.cache | sx tcp --json -p 1-65535 172.23.74.125
    ```
  * UDP Scan
    ```
    cat arp.cache | sx udp --json -p 1-65535 172.23.74.125
    ```

* Task 4. Explore Various Network Scanning Techniques using NMAP
  * Download Tools : https://nmap.org/zenmap
  * Install zenmap.exe
  * TCP ports and services
    ```
    nmap -sT -v 172.23.74.125
    ```
  * TCP stealth scan or TCP half-open scan
    ```
    nmap -sS -v 172.23.74.125
    ```
  * Xmas Scan
    ```
    nmap -sX -v 172.23.74.125
    ```
  * TCP Maimon Scan
    ```
    nmap -sM -v 172.23.74.125
    ```
  * ACK Flag Probe Scan
    ```
    nmap -sA -v 172.23.74.125
    ```
  * UDP Scan
    ```
    nmap -sU -v 172.23.74.125 -> Profile : intense scan
    ```
  * Scan Options
    ```
    nmap -sN -T4 -A -v 172.23.74.125
    ```
  * IDLE/IPID Header Scan
    ```
    nmap -sI -v 172.2374.125
    ```
  * SCTP INTI Scan
    ```
    nmap -sY -v 172.2374.125
    ```
  * SCTP COOKIE ECHO Scan
    ```
    nmap -sZ -v 172.2374.125
    ```
  * Detect Service Version
    ```
    nmap -sV 172.2374.125
    ```
  * Scan Asterisk
    ```
    nmap -A 172.23.74.*
    ```

* Task 5. Explore Various Network Scanning Techniques using Hping3

