## Overview
### Module 1. Methodology Certified Ethical Hacker
* A. Explain Information Security Concepts
  * Elements of Information Security
       * Confidentiality
       * Integrity
       * Availability
       * Authenticity
       * Non-Repudiation
      
  * Motives, Goals, And Objectives of Information Security Attacks
       
  * Classification of Attacks
       * Passive Attacks
       * Active Attacks
       * Close-in Attacks
       * Insider Attacks
       * Distribution Attacks
      
  * Information Warfare
    
* B. Explain Hacking Methodologies and Frameworks
  * 1. Hacking Methodologies and Frameworks
       
  * 2. CEH Hacking Methodology (CHM)
       * Footprinting
       * Scanning
       * Enumeration
       * Vulnerability Analysis
       * Gaining Access
         * Cracking Passwords
         * Vulnerability Exploitation
       * Escalating Privileges
       * Maintaining Access
         * Executing Applications
         * Hiding Files
       * Clearing Logs
         * Covering Tracks
        
  * 3. Cyber Kill Chain Methodology
       * Reconnaissance
       * Weaponization
       * Delivery
       * Exploitation
       * Installation
       * Command and Control
       * Actions on Objectives
      
  * 4. Tactics, Techniques, and Procedures (TTPs)
  
  * 5. Adversary Behavioral Identification
       * Internal Reconnaisance
       * Use of PowerShell
       * Unspecified Proxy Activities
       * Use of Command-Line Interface
       * HTTP User Agent
       * Command and Control Server
       * Use of DNS Tunneling
       * Use of Web Shell
       * Data Staging
      
  * 6. Indicators of Compromise (IoCs)
       
  * 7. Categories of Indicators of Compromise
       * Email Indicators
       * Network Indicators
       * Host-Based Indicators
       * Behavioral Indicators
      
  * 8. MITRE ATT&CK Framework
       * Reconnaissance
       * Resource Development
       * Intial Access
       * Execution
       * Persistence
       * Privilege Escalation
       * Defense Evasion
       * Credential Access
       * Discovery
       * Lateral Movement
       * Collection
       * Command and Control
       * Exfiltration
       * Impact

  * 9. Diamond Model of Intrusion Analysis
       * Adversary
       * Victim
       * Capability
       * Infrastructure
   
  * 10. Additional Event Meta-Features
        * Timestamp
        * Phase
        * Result
        * Direction
        * Methodology
        * Resource
      
  * 11. Extended Diamond Model
        * Socio-policital meta-feature
        * Technology meta-feature
    

* C. Explain Hacking Concepts and Diiferent Hacker Classes
* D. Explain Ethical Hacking Concepts and Scope
* E. Summarize the Techniques used in Information Security Controls
* F. Explain the Importance of Applicable Security Laws and Standards

### Module 2. Footprinting and Reconnaissance
*  A. Footprinting Search Engine
   * Online Tools
     * Google Search Engines
     * Mattw : https://mattw.io/youtube-metadata
     * Search FTPs : https://searchftps.net
     * Shodan : https://shodan.io

*  B. Footprinting Web Services
   * Online Tools
     * Netcraft : https://sitereport.netcraft.com
     * Peekyou : https://peekyou.com
     * Censys : https://search.censys.io
   * Package Tools
     * theHarvester : https://github.com/laramies/theHarvester
     * TOR Browser : https://torproject.org/download
       
*  C. Footprinting Social Engineering Sites
   * Online Tools
     * FollowerWonk : https://www.followerwonk.com/analyze
   * Package Tools
     * theHarvester : https://github.com/laramies/theHarvester
     * sherlock : https://github.com/sherlock-project/sherlock
       
*  D. Website Footprinting
   * Online Tools
     * CentralOps : https://www.centralops.net
   * Package Tools
     * Ping
     * Photon : https://github.com/s0md3v/Photon.git
     * theHarvester : https://github.com/laramies/theHarvester
     * sherlock : https://github.com/sherlock-project/sherlock
     * Web Data Extractor : https://web-data-extractor.apponic.com/
     * HTTrack Website Copier : https://www.httrack.com
     * GRecon : https://github.com/Moh-Gebril/grecon.git
     * CeWL : https://github.com/digininja/CeWL
       
*  E. Email Footprinting
   * Package Tools
     * eMailTrackerPro : https://emailtracker.website/pro
       
*  F. Whois Footprinting
   * Online Tools
     * DomainTools : https://whois.domaintools.com
       
*  G. DNS Footprinting
   * Online Tools
     * Kloth : https://kloth.net
   * Package Tools
     * Nslookup
       
*  H. Perform Network Footprinting
   * Online Tools
     * American Registry for Internet Numbers : https://www.arin.net
   * Package Tools
     * Nslookup
     * Traceroute
       
*  I. Perform Footprinting using Footprinting Tools
   * Online Tools
     * OSINT Framework : https://www.osintframework.com 
   * Package Tools
     * Recon-ng : https://github.com/lanmaster53/recon-ng
     * Maltego : https://www.maltego.com/
     * OSRFramework : https://www.kali.org/tools/osrframework/
     * FOCA : https://github.com/ElevenPaths/FOCA.git
     * BillCiper : https://github.com/bahatiphill/BillCipher.git
     * Recon-dog : https://github.com/s0md3v/ReconDog
     * GRecon : https://github.com/Moh-Gebril/grecon.git
     * Th3Inspector : https://github.com/moham3driahi/th3inspector
     * Raccon : https://github.com/nettitude/raccoon
     * Orb : https://github.com/epsylon/orb
       
### Module 3. Scanning Networks
*  A. Perform Host Discovery
   * Package Tools
     * NMAP : https://nmap.org/download
     * Angry IP Scanner : https://angryip.org/download/#windows
       
*  B. Perform Port and Services Discovery
   * Package Tools
     * MegaPing : https://magnetsoft.com/producs-download
     * NetScanTools Pro : https://netscantools.com/ntbasicrequestform.html
     * SX : https://github.com/v-byte-cpu/sx
     * Zenmap : https://nmap.org/zenmap
     * Hping3 : https://github.com/antirez/hping
       
*  C. Perform OS Discovery
   * Package Tools
     * Wireshark : https://www.wireshark.org/download.html
     * NMAP : https://nmap.org/download
     * Unicornscan : https://www.kali.org/tools/unicornscan/
       
*  D. Scan Beyond IDS and Firewall (Techniques to Evade IDS/Firewall)
   * Package Tools
     * NMAP : https://nmap.org/download
     * Colasoft Packet Builder : https://www.colasoft.com/download/products/download_packet_builder.php
     * Hping3 : https://github.com/antirez/hping
     * NetScanTools Pro : https://netscantools.com/ntbasicrequestform.html
       
*  E. Perform Network Scanning using Various Scanning Tools
   * Package Tools
     * Metasploit : https://www.metasploit.com/
       

### Module 4. Enumeration
*  A. Perform NetBIOS Enumeration
   * Package Tools
     * Nbtstat
     * NetBIOSEnumerator : https://nbtenum.sourceforge.net/
     * NMAP : https://nmap.org/download
     * Global Network Inventory : https://magnetosoft.com/product-global-network-inventory/
     * Advanced IP Scanner : https://angryip.org/download/#windows
     * Hyena : https://www.systemtools.com/hyena/download.htm
     * Nsauditor Network Security Auditor : https://www.nsauditor.com/

*  B. Perform SNMP Enumeration
   * Package Tools
     * NMAP : https://nmap.org/download
     * Snmp-check : https://www.kali.org/tools/snmpcheck/
     * SoftPerfect Network Scanner : https://www.softperfect.com/products/networkscanner/
     * SnmpWalk : https://www.kali.org/tools/net-snmp/
     
*  C. Perform LDAP Enumeration
   * Package Tools
     * ADExplorer : https://live.sysinternals.com/ADExplorer.exe
     * NMAP : https://nmap.org/download
     * Python : https://www.python.org/
     * ldapsearch : https://github.com/dinigalab/ldapsearch
     
*  D. Perform NFS Enumeration
   * Package Tools
     * NMAP : https://nmap.org/download
     * Superenum : https://github.com/p4pentest/SuperEnum.git
     * RPCScan : https://github.com/hegusung/RPCScan.git
     
*  E. Perform DNS Enumeration
   * Package Tools
     * Dig
     * Nslookup
     * dnsrecon : https://www.kali.org/tools/dnsrecon/
     * NMAP : https://nmap.org/download
     * LDNS : https://github.com/NLnetLabs/ldns
     * nsec3map : https://github.com/anonion0/nsec3map
     * nsec3walker : https://github.com/unsecured-company/nsec3walker
     * DNSwalk : https://www.kali.org/tools/dnswalk/
     
*  F. Perform SMTP Enumeration
   * Package Tools
     * NMAP : https://nmap.org/download
     
*  G. Perform RPC, SMB and FTP Enumeration
   * Package Tools
     * NetScanTools : https://www.netscantools.com/nstprodemorequestform.html
     * NMAP : https://nmap.org/download
     
*  H. Perform Enumeration using Various Enumeration Tools
   * Package Tools
     * Global Network Inventory : https://magnetosoft.com/product-global-network-inventory/
     * Angry IP Scanner : https://angryip.org/download/#windows
     * Enum4linux : https://www.kali.org/tools/enum4linux/

### Module 5. Vulnerability Analysis
*  A. Perform Vulnerability Research with Vulnerability Scoring Systems and Databases
   * Online Databases 
     * Common Weakness Enumeration (CWE) : https://cwe.mitre.org/find/index.html
     * Common Vulnerability and Exposures (CVE) : https://cve.mitre.org
     * National Vulnerability Database (NVD) : https://nvd.nist.gov
       
*  B. Perform Vulnerability Assessment using Various Vulnerability Assessment Tools
   * Package Tools
     * OpenVAS : https://www.greenbone.net/en/openvas-free/
     * Nessus : https://www.tenable.com/downloads/nessus?loginAttempted=true
     * GFI LanGuard : https://gfi.ai/products-and-solutions/network-security-solutions/gfi-languard/download/
       
*  C. Perform Web Servers and Application Vulnerability Scanning using CGI Scanner Nikto
   * Package Tools
     * Nikto : https://github.com/sullo/nikto
       
### Module 6. System Hacking

### Module 7. Malware Threats
* A. Gain Access to Target System using Trojans
  * Malware Tools
    * njRAT (Build Malware) : https://github.com/alyaparan/NjRat-0.7D
    * SwayzCryptor (Encrypt Malware) :
    * TheefRAT Trojan v2.10 (Server Trojan) :
      
* B. Infect Target System using Virus
  * Malware Tools
    * JPS Virus Maker : https://github.com/Hackalyze-Tools/jps-virus-maker
      
* C. Perform Static Malware Analysis
  * Online Tools
    * Hybrid Analysis : https://hybrid-analysis.com
    * Virus Total : https://virustotal.com
    * Valkyrie : https://valkryrie.comodo.com
    * Cuckoo Sandbox : https://cuckoosandbox.org
    * Jotti : https://virusscan.jotti.org
    * IObit Cloud : https://cloud.iobit.com
      
  * Package Tools
    * BinText 3.0.3 : https://www.oldergeeks.com/downloads/file.php?id=2441
    * FLOSS : https://fireeye.com
    * Strings : https://learn.microsoft.com/en-us/sysinternals/downloads/strings
    * Free EXE DLL Resource Extract : https://resourceextract.com
    * FileSeek : https://fileseek.ca
    * PEid : https://github.com/wolfram77web/app-peid
    * DIE : https://github.com/horsicq/DIE-engine/releases
    * PE explorer : https://www.pe-explorer.com/
    * Portable Executable Scanner (Pescan) : https://tzworks.net
    * Resource Hacker : https://angusj.com
    * PEView : https://aldeid.com
    * Dependency Walker : https://www.dependencywalker.com/
    * Dependency-check : https://jeremylong.github.io
    * Snyk : https://synk.io
    * RetrireJS : https://retirejs.github.io
    * IDA Freeware : https://hex-rays.com/ida-free
    * OllyDbg : https://www.ollydbg.de/download.htm
    * Ghidra : https://github.com/NationalSecurityAgency/ghidra/releases
    * Radare2 : https://rada.re
    * WinDbg : https://windbg.org
    * ProcDump : https://learn.microsoft.com/en-us/sysinternals/downloads/procdump
    
* D. Perform Dynamic Malware Analysis
  * Package Tools
    * TCPView : https://www.sysinternals.com
    * CurrPorts : https://www.nirsoft.net/utils/cports.html#DownloadLinks
    * ProcessMonitor : https://learn.microsoft.com/en-us/sysinternals/downloads/procmon
    * Reg Organizer : https://www.chemtable.com/organizer.htm
    * Regshot : https://sourceforge.net/projects/regshot/
    * Registry Viewer : https://accessdata.com
    * RegScanner : https://nirsoft.com
    * Registrar Registry Manager : https://resplendence.com
    * Windows Service Manager : https://sysprogs.com/legacy/tools/srvman/
    * Autoruns : https://learn.microsoft.com/en-us/sysinternals/downloads/autoruns
    * WinPatrol : https://www.winpatrol.online/
    * Autorun Organizer : https://chemtable.com
    * Quick Startup : https://glarysoft.com
    * Chameleon Startup Manager : https://chameleon-managers.com
    * Mirekusoft Install Monitor : https://www.mirekusoft.com/
    * Tripwire File Integrity and Change Manager : https://tripwire.com
    * Netwrix Auditor : https://netwrix.com
    * Verisys : https://ionx.co.uk
    * CSP Checker : https://cspsecurity.com
    * Driver View : https://www.nirsoft.net/utils/driverview.html
    * Driver Reviver : https://www.reviversoft.com/driver-reviver/
    * Driver Bosster : https://iobit.com
    * Driver Easy : https://drivereasy.com
    * Driver Fusion : https://treexy.com
    * Driver Genius 22 : https://driver-soft.com
    * ProcessMonitor : https://learn.microsoft.com/en-us/sysinternals/downloads/procmon
    * DNSQuery Sniffer : https://www.nirsoft.net/utils/dns_query_sniffer.html
    * DNSstuff : https://dnsstuff.com/freetools
    * SonarLite : https://constellix.com
