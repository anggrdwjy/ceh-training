## Outline

### Module 2. Footprinting and Reconnaissance

#### A. Footprinting Search Engine
#### B. Footprinting Web Services
#### C. Footprinting Social Engineering Sites

#### D. Website Footprinting
* Task 1. Gather Information About Target using PING CMD
  * Testing
  ```
  ping example.com
  ping example.com -f 1400
  ping example.com -f -l 1300
  ping example.com -i 3 
  ping example.com -i 2 -n 1
  ping 10.0.0.1 
  ping 10.0.0.1 -f -l 1300
  ping 10.0.0.1 -f 1400
  ping 10.0.0.1 -i 3
  ping 10.0.0.1 -i 2 -n 1
  ```
    
* Task 2. Gather Information About Target Website using Photon
  * Install from Github : https://github.com/s0md3v/Photon.git
  * Running Tools
    ```
    ┌──(root㉿kali)-[/home/kali/Photon]
    └─# python3 photon.py -u awc.my.id -l 3 -t 200 --wayback
    /home/kali/Photon/photon.py:19: SyntaxWarning: invalid escape sequence '\/'
      / %s__%s \/ /_  ____  / /_____  ____
          ____  __          __
         / __ \/ /_  ____  / /_____  ____
        / /_/ / __ \/ __ \/ __/ __ \/ __ \
       / ____/ / / / /_/ / /_/ /_/ / / / /
      /_/   /_/ /_/\____/\__/\____/_/ /_/ v1.3.2
    
    [~] Fetching URLs from archive.org
    [+] Retrieved -1 URLs from archive.org
    [+] URLs retrieved from robots.txt: 1
    [~] Level 1: 2 URLs
    [!] Progress: 2/2
    [~] Crawling 0 JavaScript files
    
    --------------------------------------------------
    [+] Robots: 1
    [+] Internal: 2
    [+] External: 3
    --------------------------------------------------
    [!] Total requests made: 3
    [!] Total time taken: 0 minutes 6 seconds
    [!] Requests per second: 0
    [+] Results saved in awc.my.id directory
    
    ┌──(root㉿kali)-[/home/kali/Photon]
    └─#
    ```
    
  * Open Result Folder
    * /photon/example.com/internal.txt
    * /photon/example.com/external.txt
    * /photon/example.com/robots.txt
      
* Task 3. Gather Information About Target Website using Central Ops
  * Search Domain Target from Online Tools : https://www.centralops.net
  
* Task 4. Extract Company Data using Web Data Extractor
  * Search Web Data Extractor 8.3 [Outdated]

* Task 5. Mirror Target Website using HTTrack Website Copier
  * Download from : https://www.httrack.com
  * Running Tools
    * Create Project -> Input Domain
    * Set Options -> Scan Rules -> Checklist [jpg,gif,cgi-bin,cgi]
    * Finish
      
* Task 6. Gather Information About Target Website using GRecon
  * Install form Github : https://github.com/Moh-Gebril/grecon.git
  * Running Tools
    ```
    ┌──(root㉿kali)-[/home/kali/grecon]
    └─# python3 grecon_cli.py -t awcloud.my.id --nmap --nse
    
         ██████╗ ██████╗ ███████╗ ██████╗ ██████╗ ███╗   ██╗
        ██╔════╝ ██╔══██╗██╔════╝██╔════╝██╔═══██╗████╗  ██║
        ██║  ███╗██████╔╝█████╗  ██║     ██║   ██║██╔██╗ ██║
        ██║   ██║██╔══██╗██╔══╝  ██║     ██║   ██║██║╚██╗██║
        ╚██████╔╝██║  ██║███████╗╚██████╗╚██████╔╝██║ ╚████║
         ╚═════╝ ╚═╝  ╚═╝╚══════╝ ╚═════╝ ╚═════╝ ╚═╝  ╚═══╝
    
    ================================================================================
      GRecon v1.0.0 - Advanced Network Reconnaissance Tool
      Author: Mohamed Gebril
      GitHub: https://github.com/Moh-Gebril/grecon
      Running on: Linux 6.18.5+kali-amd64
    ================================================================================
      Scan initiated at: 2026-03-31 13:23:55
    ================================================================================
    
    --------------------------------------------------------------------------------
      Target: awcloud.my.id
      Time started: 2026-03-31 13:23:55
    --------------------------------------------------------------------------------
    
    2026-03-31 13:23:55,910 - grecon.core.scanner - INFO - Starting scan of 172.67.179.243 (awcloud.my.id)
    2026-03-31 13:23:55,910 - grecon.core.scanner - INFO - Port range: 1-65535
    2026-03-31 13:23:55,910 - grecon.core.scanner - INFO - Using 200 threads
    2026-03-31 13:23:56,585 - grecon.core.scanner - INFO - Port 443 is open
    Port 443 is open
    2026-03-31 13:23:59,001 - grecon.core.scanner - INFO - Port 2052 is open
    Port 2052 is open
    2026-03-31 13:23:59,024 - grecon.core.scanner - INFO - Port 2053 is open
    Port 2053 is open
    2026-03-31 13:23:59,024 - grecon.core.scanner - INFO - Port 2083 is open
    Port 2083 is open
    2026-03-31 13:23:59,025 - grecon.core.scanner - INFO - Port 2087 is open
    Port 2087 is open
    2026-03-31 13:23:59,025 - grecon.core.scanner - INFO - Port 2086 is open
    Port 2086 is open
    2026-03-31 13:23:59,025 - grecon.core.scanner - INFO - Port 2095 is open
    Port 2095 is open
    2026-03-31 13:23:59,026 - grecon.core.scanner - INFO - Port 2096 is open
    Port 2096 is open
    2026-03-31 13:23:59,026 - grecon.core.scanner - INFO - Port 2082 is open
    Port 2082 is open
    ^C
    
    Scan interrupted by user. Exiting...
    
    ┌──(root㉿kali)-[/home/kali/grecon]
    └─#
    ```
    
 * Task 7. Gather Wordlist from Target Website using CeWL
   * Running Tools
     ```
     ┌──(root㉿kali)-[/home/kali]
     └─# cewl -w wordlist.txt -d 2 -m 5 awcloud.my.id
     CeWL 6.2.1 (More Fixes) Robin Wood (robin@digi.ninja) (https://digi.ninja/)
     
     ```
   * Save Wordlist
     ```
     ┌──(root㉿kali)-[/home/kali]
     └─# cat wordlist.txt
     server
     Cloudflare
     awcloud
     Error
     information
     Working
     website
     owner
     Contact
     hosting
     provider
     letting
     responding
     Additional
     troubleshooting
     Click
     reveal
     Performance
     security
     error
     footer
     minutes
     again
     Please
     visitor
     displaying
     result
     connection
     returning
     happened
     Singapore
     Browser
     cloudflare
     Visit
     
     ┌──(root㉿kali)-[/home/kali]
     └─#

     ```
    
#### E. Email Footprinting
* Task 1. Perform Email Footprinting
  * Install eMailTrackerPro.exe [Outdated]

#### F. Whois Footprinting
* Task 1. Perform Whois Lookup using DomainTools
  * Search Domain Target from Online Tools : https://whois.domaintools.com

#### G. DNS Footprinting
* Task 1. Gather DNS Information using NSLOOKUP
  ```
  C:\Users\Administrator>nslookup
  Default Server:  UnKnown
  Address:  192.168.1.1
  > set type=a
  > awcloud.my.id
  Server:  UnKnown
  Address:  192.168.1.1
  Non-authoritative answer:
  Name:    awcloud.my.id
  Addresses:  104.21.31.205
            172.67.179.243
  > set type=cname
  > awcloud.my.id
  Server:  UnKnown
  Address:  192.168.1.1
  awcloud.my.id
          primary name server = cecelia.ns.cloudflare.com
          responsible mail addr = dns.cloudflare.com
          serial  = 2397555721
          refresh = 10000 (2 hours 46 mins 40 secs)
          retry   = 2400 (40 mins)
          expire  = 604800 (7 days)
          default TTL = 1800 (30 mins)
  > set type=a
  > cecelia.ns.cloudflare.com
  Server:  UnKnown
  Address:  192.168.1.1
  
  Non-authoritative answer:
  Name:    cecelia.ns.cloudflare.com
  Addresses:  172.64.34.135
            108.162.194.135
            162.159.38.135
  >
  ```
* Task 2. Gather DNS Information using Online Tools
  * Search Domain Target from Online Tools : https://kloth.net

#### H. Perform Network Footprinting
* Task 1. Traceroute from Online Tools : https://www.arin.net
  
* Task 2. Traceroute from CMD
  ```
  tracert 103.xx.yy.zz
  tracert -h 5 103.xx.yy.zz
  ```
  
* Task 3. Traceroute from Linux
  ```
  traceroute 103.xx.yy.zz
  ```
  
#### I. Perform Footprinting using Footprinting Tools
* Task 1. Footprinting Target using Recon-ng
  * Install Recon-ng
  ```
  apt install recon-ng -y
  ```
  * Running Tools
  ```
    ┌──(root㉿kali)-[/home/kali]
  └─# recon-ng
  [*] Version check disabled.
  
      _/_/_/    _/_/_/_/    _/_/_/    _/_/_/    _/      _/            _/      _/    _/_/_/
     _/    _/  _/        _/        _/      _/  _/_/    _/            _/_/    _/  _/
    _/_/_/    _/_/_/    _/        _/      _/  _/  _/  _/  _/_/_/_/  _/  _/  _/  _/  _/_/_/
   _/    _/  _/        _/        _/      _/  _/    _/_/            _/    _/_/  _/      _/
  _/    _/  _/_/_/_/    _/_/_/    _/_/_/    _/      _/            _/      _/    _/_/_/
  
  
                                            /\
                                           / \\ /\
      Sponsored by...               /\  /\/  \\V  \/\
                                   / \\/ // \\\\\ \\ \/\
                                  // // BLACK HILLS \/ \\
                                 www.blackhillsinfosec.com
  
                    ____   ____   ____   ____ _____ _  ____   ____  ____
                   |____] | ___/ |____| |       |   | |____  |____ |
                   |      |   \_ |    | |____   |   |  ____| |____ |____
                                     www.practisec.com
  
                        [recon-ng v5.1.2, Tim Tomes (@lanmaster53)]
  
  [91] Recon modules
  [8]  Reporting modules
  [4]  Import modules
  [2]  Exploitation modules
  [2]  Discovery modules
  [2]  Disabled modules
  
  [recon-ng][default] >
  ```
  * Optional
  ```
  recon-ng
  recon-cli
  recon-web
  ```
  
* Task 2. Footprinting using Maltego
  * Install Maltego GUI
  * Create New Graph -> Domain -> All Transform
  * Advanced
    - to DNS Name (Authority, MX, NS)
    - to IP Address
    - to Location
    - to Domain
    - to Entities Whois
      
* Task 3. Footprinting Target using OSRFramework
  * Install OSRFramework
  ```
  apt install osrframework -y
  ```
  * Running Tools
  ```
    ┌──(root㉿kali)-[/home/kali]
  └─# domainfy -n example.com -t all
  
  
          .===========================================================.
          |...........................................................|
          |...........................................................|
          |...........................................................|
          |.......................              ......................|
          |...................                    ....................|
          |...................                      ..................|
          |..................                       ..................|
          |..................                        .................|
          |..................                       ..................|
          |..................                      ...................|
          |..................                      ...................|
          |..................                      ...................|
          |.................                         .................|
          |.................                        ..................|
          |..................                       ..................|
          |...................                    ....................|
          |....................                   ....................|
          |....................                  .....................|
          |......................               ......................|
          |......................               ......................|
          |.....................                 .....................|
          |.....................                 .....................|
          |....................                   ....................|
          |..................                       ..................|
          |..............                               ..............|
          |..........                                       ..........|
          |......                                               ......|
          |....                OSRFramework 0.20.5                ....|
          |..                                                       ..|
          '==========================================================='
  
  
  
       ___  ____  ____  _____                                            _
      / _ \/ ___||  _ \|  ___| __ __ _ _ __ ___   _____      _____  _ __| | __
     | | | \___ \| |_) | |_ | '__/ _` | '_ ` _ \ / _ \ \ /\ / / _ \| '__| |/ /
     | |_| |___) |  _ <|  _|| | | (_| | | | | | |  __/\ V  V / (_) | |  |   <
      \___/|____/|_| \_\_|  |_|  \__,_|_| |_| |_|\___| \_/\_/ \___/|_|  |_|\_\
  
  
                     Coded with ♥ by Yaiza Rubio & Félix Brezo
  
  
       -- In 'domainfy', use '-t cc' to find domains resolving to ccTLDs. --
  
  
      Domainfy | Copyright (C) Yaiza Rubio & Félix Brezo (i3visio) 2014-2021
  
  This program comes with ABSOLUTELY NO WARRANTY. This is free software, and you
  are welcome to redistribute it under certain conditions. For additional info,
  visit <https://www.gnu.org/licenses/agpl-3.0.txt>.
  
  2026-03-31 12:34:30.325647      Trying to get information about 869 domain(s)…
  
          Note that a full '-t all' search may take around 3.5 mins. If that's too
          long for you, try narrowing the search using '-t cc' or similar arguments.
          Otherwise, just wait and keep calm!
  
          Press <Ctrl + C> to stop...
  
  ```
  * Optional
  ```
  searchfy -q "example.com"
  usufy --info
  mailfy --info
  phonefy --info
  entify --info
  ```
* Task 4. Footprinting Target using FOCA
  * Download from Github : https://github.com/ElevenPaths/FOCA.git
  * Microsoft Windows (64 bits). Versions 7, 8, 8.1 and 10.
  * Microsoft .NET Framework 4.7.1.
  * Microsoft Visual C++ 2010 x64 or greater.
  * An instance of SQL Server 2014 or greater.
  
* Task 5. Footprinting Target using BillCiper
  * Download from Github : https://github.com/bahatiphill/BillCipher.git
  * Running Tools
    ```
    ┌──(root㉿kali)-[/home/kali/BillCipher]
    └─# python3 billcipher.py
     ######                   #####
     #     # # #      #      #     # # #####  #    # ###### #####
     #     # # #      #      #       # #    # #    # #      #    #
     ######  # #      #      #       # #    # ###### #####  #    #
     #     # # #      #      #       # #####  #    # #      #####
     #     # # #      #      #     # # #      #    # #      #   #
     ######  # ###### ######  #####  # #      #    # ###### #    # 2.1
     Information Gathering tool for a Website or IP address
    
    Are you want to collect information of website or IP address? [website/IP]:     ^P
    ?
    Are you want to collect information of website or IP address? [website/IP]: IP
    Enter the IP address (or domain to get IP address of this domain): 1.1.1.1
    The IP address of target is: 1.1.1.1
    
     1) DNS Lookup                 13) Host DNS Finder
     2) Whois Lookup               14) Reserve IP Lookup
     3) GeoIP Lookup               15) Email Gathering (use Infoga)
     4) Subnet Lookup              16) Subdomain listing (use Sublist3r)
     5) Port Scanner               17) Find Admin login site (use Breacher)
     6) Page Links                 18) Check and Bypass CloudFlare (use HatCloud)
     7) Zone Transfer              19) Website Copier (use httrack)
     8) HTTP Header                20) Host Info Scanner (use WhatWeb)
     9) Host Finder                21) About BillCipher
     10) IP-Locator                22) Fuck Out Of Here (Exit)
     11) Find Shared DNS Servers
     12) Get Robots.txt
    
    ```
* Task 6. Footprinting Target using OSINT Framework
  * Access Website : https://www.osintframework.com
* Allternative Tools
  * Recon-dog
  * GRecon
  * Th3Inspector
  * Raccon
  * Orb


