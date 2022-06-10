This diff adds support for reading the PJSIPEXTERNALFQDN environment variable and using that in INVITE and VIA headers instead of having to hard code it in the source code and recompile every time. Use the associated systemd service file to easily set and update that environment variable.

Inbound calls, outbound calls, transferred calls all appear to work properly.
"Consult then transfer" calls do not currently work, but that's a different Asterisk problem unrelated to the FQDN issue.