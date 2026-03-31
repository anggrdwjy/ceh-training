## Outline

### Module 2. Footprinting and Reconnaissance

#### A. Footprinting Search Engine
#### B. Footprinting Web Services
#### C. Footprinting Social Engineering Sites
#### D. Website Footprinting
#### E. Email Footprinting
#### F. Whois Footprinting
#### G. DNS Footprinting
#### H. Perform Network Footprinting
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


