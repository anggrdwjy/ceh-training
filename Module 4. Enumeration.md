## Module 4. Enumeration

#### A. Perform NetBIOS Enumeration
* Task 1. Perform NetBIOS Enumeration using CMD
  * Display NetBIOS name table of remote computer
    ```
    nbtstat -a 10.13.3.55
    ```
  * Unauthenticated session
    ```
    nbtstat -c
    ```
  * Connection status, shared folder and network information
    ```
    net use
    ```
* Task 2. Perform NetBIOS Enumeration using NetBIOS Enumeration
  * Download NetBIOSEnumerator.exe : https://nbtenum.sourceforge.net/

* Task 3. Perform NetBIOS Enumeration using NMAP NSE Script
  * NetBIOS Services Version
    ```
    nmap -sV -v --script nbtstat.nse 172.23.74.125
    ```
  * NetBIOS UDP Enumeration
    ```
    nmap -sU -p 137 --script nbtstat.nse 172.23.74.125
    ```
* Optional Tools
	* Global Network Inventory
	* Advanced IP Scanner
	* Hyena
	* Nsauditor Network Security Auditor

#### B. Perform SNMP Enumeration
* Task 1. Perform SNMP Enumeration using snmp-check
  * SNMP UDP Scanner
    ```
    nmap -sU -p 161 172.23.74.125
    ```
  * SNMP Enumeration
    ```
    snmp-check 172.23.74.125
    ```
    
* Task 2. Perform SNMP Enumeration using SoftPerfect Network Scanner
  * Download SoftPerfect Network Scanner : https://www.softperfect.com/products/networkscanner/
  * Open SoftPerfect Network Scanner
  * Options -> Remote SNMP -> Mark All/None
  * Start Scanning
    
* Task 3. Perform SNMP Enumeration using SnmpWalk
  * Specifies SNMP version 1
    ```
    snmpwalk -v1 -c public 172.23.74.125
    ```
  * Specifies SNMP version 2
    ```
    snmpwalk -v2c -c public 172.23.74.125
    ```

* Task 4. Perform SNMP Enumeration using NMAP
  * SNMP UDP System Description
    ```
    nmap -sU -p 161 --script=snmp-sysdescr 172.23.74.125
    ```
  * SNMP UDP Processes
    ```
    nmap -sU -p 161 --script=snmp-processes 172.23.74.125
    ```
  * SNMP UDP Win32 Software
    ```
    nmap -sU -p 161 --script=snmp-win32-software 172.23.74.125
    ```
  * SNMP UDP Interfaces
    ```
    nmap -sU -p 161 --script=snmp-interfaces
    ```

#### C. Perform LDAP Enumeration
* Task 1. Perform LDAP Enumeration using AD Explorer
  * Download ADExplorer.exe : https://live.sysinternals.com/ADExplorer.exe
  * Connect to Active Directory

* Task 2. Perform LDAP Enumeration using Python and NMAP
  * LDAP UDP Scanner
    ```
    nmap -sU -p 389 172.23.74.125
    ```
  * LDAP Bruteforce Username Enumeration
    ```
    nmap -p 389 --script ldap-brute --script.args ldap.base='"cn=users,dc=Windows,dc=com"' 172.23.74.125
    ```
  * Manual LDAP Enumeration
    ```
    python3
    >>> import ldap3
    >>> server=ldap3.server('172.23.74.125',get_info=ldap3.ALL,port=389)
    >>> connection=ldap3.Connection(server)
    >>> connection.bind()
    >>> server.info
    >>> connection.search(search_base='DC=CEH,DC=com',search_filter='(&(objectclass=*))',search_scope='SUBTREE',attributes='*')
    >>> connection.entries
    >>> connection.search(search_base='DC=CEH,DC=com',search_filter='(&(objectclass=person))',search_scope='SUBTREE',attributes='userpassword') 
    >>> connection.entries
    ```

* Task 3. Perform LDAP Enumeration using ldapsearch
  * LDAP Gather Details
    ```
    ldapsearch -h 172.23.74.125 -x -s base namingcontexts
    ```
  * LDAP More Information
    ```
    ldapsearch -h 172.23.74.125 -x -b "DC=Windows,DC=com"
    ```
  * LDAP Directory Tree
    ```
    ldapsearch -x -h 172.23.74.125 -b "DC=Windows,DC=com" "objectclass=*"
    ```

#### D. Perform NFS Enumeration
* Task 1. Perform NFS Enumeration using RPCScan and SuperEnum
  * NFS service Scanner
    ```
    nmap -p 2049 172.23.74.125
    ```
  * Download Superenum : https://github.com/p4pentest/SuperEnum.git
    ```
    ┌──(root㉿kali)-[/home/kali/superenum/SuperEnum]
    └─# ./superenum target.txt
    Enter IP List filename with path
    target.txt
    
    TCP Scan Started for IP: 172.23.74.125
    
    UDP Scan Started for IP: 172.23.74.125
    
    Testing for 172.23.74.125: 3389
    Testing for 172.23.74.125: 3389, Tool: nmap_rdp-enum-encryption
    Testing for 172.23.74.125: 3389, Tool: nmap_rdp-vuln-ms12-020
    ```
  * Download RPCScan : https://github.com/hegusung/RPCScan.git
    ```
    python3 rpc-scan.py 172.23.74.125 --rpc
    ```

#### E. Perform DNS Enumeration
* Task 1. Perform DNS Enumeration using Zone Transfer
  * Answer Section
    ```
    ┌──(root㉿kali)-[/home/kali]
    └─# dig ns www.awcloud.my.id
    
    ; <<>> DiG 9.20.18-1-Debian <<>> ns www.awcloud.my.id
    ;; global options: +cmd
    ;; Got answer:
    ;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 50355
    ;; flags: qr rd ra; QUERY: 1, ANSWER: 0, AUTHORITY: 1, ADDITIONAL: 1
    
    ;; OPT PSEUDOSECTION:
    ; EDNS: version: 0, flags:; udp: 1232
    ;; QUESTION SECTION:
    ;www.awcloud.my.id.             IN      NS
    
    ;; AUTHORITY SECTION:
    awcloud.my.id.          1800    IN      SOA     cecelia.ns.cloudflare.com. dns.cloudflare.com. 2397555721 10000 2400 604800 1800
    
    ;; Query time: 64 msec
    ;; SERVER: 1.1.1.1#53(1.1.1.1) (UDP)
    ;; WHEN: Wed Apr 01 05:09:03 EDT 2026
    ;; MSG SIZE  rcvd: 111
    
    ```
  * Axfr Retrieving DNS 
    ```
    ┌──(root㉿kali)-[/home/kali]
    └─# dig @cecelia.ns.cloudflare.com www.awcloud.my.id axfr
    
    ; <<>> DiG 9.20.18-1-Debian <<>> @cecelia.ns.cloudflare.com www.awcloud.my.id axfr
    ; (6 servers found)
    ;; global options: +cmd
    ; Transfer failed.
    
    ```
  * NSLOOKUP Interactive Mode
    ```
    C:\Users\Administrator>nslookup
    Default Server:  UnKnown
    Address:  10.13.3.0
    
    > set querytype=soa
    > awcloud.my.id
    Server:  UnKnown
    Address:  10.13.3.0
    
    Non-authoritative answer:
    awcloud.my.id
            primary name server = cecelia.ns.cloudflare.com
            responsible mail addr = dns.cloudflare.com
            serial  = 2397555721
            refresh = 10000 (2 hours 46 mins 40 secs)
            retry   = 2400 (40 mins)
            expire  = 604800 (7 days)
            default TTL = 1800 (30 mins)
    > ls -d cecelia.ns.cloudflare.com
    [UnKnown]
    *** Can't list domain cecelia.ns.cloudflare.com: Query refused
    The DNS server refused to transfer the zone cecelia.ns.cloudflare.com to your computer. If this
    is incorrect, check the zone transfer security settings for cecelia.ns.cloudflare.com on the DNS
    server at IP address 10.13.3.0.
    >
    ```

* Task 2. Perform DNS Enumeration using DNSSEC Zone Walking
  * DNSSEC Zone Enumeration
	```
	dnsrecon -d www.awcloud.my.id -z
	```
  * Optional Tools
	* LDNS
	* nsec3map
	* nsec3walker
	* DNSwalk
	
* Task 3. Perform DNS Enumeration using NMAP
  * NMAP DNS Service Discovery
	```
	nmap --script=broadcast-dns-service-discovery awcloud.my.id
	```
  * NMAP DNS Bruteforce
	```
	nmap -T4 -p 53 --script dns-brute awcloud.my.id
	```
  * NMAP DNS SRV Enumeration
	```
	nmap --script dns-srv-enum --script-args "dns-srv-enum.domain='awcloud.my.id'"
	```

#### F. Perform SMTP Enumeration
* Task 1. Perform SMTP Enumeration using NMAP
  * SMTP Enumeration User
	```
	nmap -p 25 --script=smtp-enum-users 172.23.74.125
	```
  * SMTP Open Relay
	```
	nmap -p 25 --script=smtp-open-relay 172.23.74.125
	```
  * SMTP Command Available
	```
	nmap -p 25 --script=smtp-command 172.23.74.125
	```

#### G. Perform RPC, SMB and FTP Enumeration
* Task 1. Perform SMB and RPC Enumeration using NetScanTools Pro
  * Download NetScanTools : https://www.netscantools.com/nstprodemorequestform.html

* Task 2. Perform RPC, SMB and FTP Enumeration using NMAP
  * FTP Scanner
	```
	nmap -p 21 172.23.74.125
	```
  * FTP Specifies Template
	```
	nmap -T4 -A 172.23.74.125
	```
  * FTP Host Script Results
	```
	nmap -p 445 -A 172.23.74.125
	```
  * FTP Traceroute Scanner
	```
	nmap -p 21 -A 172.23.74.125
	```

#### H. Perform Enumeration using Various Enumeration Tool
* Task 1. Enumerate Information using Global Network Inventory
  * Download Global Network Inventory : https://magnetosoft.com/product-global-network-inventory/

* Task 2. Enumerate Network Resources using Advanced IP Scanner
  * Download Angry IP Scanner : https://angryip.org/download/#windows

* Task 3. Enumerate Information using Enum4linux
  * NetBIOS Information Enumeration
	```
	┌──(root㉿kali)-[/home/kali]
	└─# enum4linux -u martin -p applu -n 172.23.74.125
	Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Wed Apr  1 06:00:44 2026
	
	 =========================================( Target Information )=========================================
	
	Target ........... 172.23.74.125
	RID Range ........ 500-550,1000-1050
	Username ......... 'martin'
	Password ......... 'applu'
	Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none
	
	
	 ===========================( Enumerating Workgroup/Domain on 172.23.74.125 )===========================
	
	
	[E] Can't find workgroup/domain
	
	
	
	 ===============================( Nbtstat Information for 172.23.74.125 )===============================
	
	```
  * Enumeration Data Target Information
	```
	enum4linux -u martin -p apple -U 172.23.74.125
	```
  * Enumeration OS Information
	```
	enum4linux -u martin -p apple -o 172.23.74.125
	```
  * Enumeration Password Policy Information
	```
	enum4linux -u martin -p apple -P 172.23.74.125
	```
  * Enumeration Group Policy Information
	```
	enum4linux -u martin -p apple -G 172.23.74.125
	```
  * Enumeration Share Policy Information
	```
	enum4linux -u martin -p apple -S 172.23.74.125
	```
    
  
