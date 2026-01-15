
# Networking - Networking Core Protocols - Report Summary

[Room Link](https://tryhackme.com/room/networkingcoreprotocols)

## Concepts and hands-on labs

[Hands-on Lab file](Assets/HandsOnRecorded.sh)

#### DNS 

DNS (Domain Name System) is a crucial TCP protocol that translates the name of the domain to IP address so that the router could forward it to the destination and retrieves it back. 

This protocol has 4 types as written on the room, here are listed:

**A**: Shows the domain name with IPv4 address, for example: `192.168.0.1`.

**AAAA**: Shows the domain name with IPv6 address, for example: `A016:FD04:C72A:0018:8B01:1021:CA92:001F`.

**CNAME**: Shows the complete domain name, for instance: `https://google.com`.

**MX**: Shows the mail server that is responsible to handling the domain.

#### WHOIS

WHOIS is a tool that is utilised for retrieving public information about the domain. It lists a number of information, such as the provider of the website, registry URL, etc.

#### HTTP(S)

HTTP (HyperText Transfer Protocol) is a networking TCP protocol that runs on a web browser. This protocol runs on port 80 and 443 for HTTPS.

#### FTP

FTP (File Transfer Protocol) is a networking protocol that functions on transferring files from client to the web server and vice versa. This protocol uses TCP and runs on port 21.

#### SMTP, POP3, IMAP

SMTP (Simple Mail Transfer Protocol), POP3, and IMAP (Internet Message Access Protocol) are protocols that are utilised for fetching, receiving, and synchronising mail messages between the server and the client. 

These protocols are running on different TCP ports simultaneously, with SMTP running on TCP with port 25, POP3 running on TCP with port 110, and IMAP running on TCP with port 143.

## Skills learned

#### Hard skills

1. Telnet
2. Whois
3. nslookup

#### Soft skill

1. Simple Problem Solving

## Conclusion 

This room covers the technical approach on how to interact with the core protocols available on the system. It is vital for users to understand as it may raise a number of vulnerabilities that are undetected in the system itself. 


