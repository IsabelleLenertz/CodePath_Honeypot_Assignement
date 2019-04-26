# CodePath_Honeypot_Assignement
## Which Honeypot(s) you deployed:
- dionaea
- elastichoney

## Any issues you encountered
At first, probing the port on my Dionaea honeypot did not show up the the attacks. I had:

>> nmap 35.239.221.133

>> Starting Nmap 6.40 ( http://nmap.org ) at 2019-04-23 21:22 UTC

>> Note: Host seems down. If it is really up, but blocking our ping probes, try -Pn

>> Nmap done: 1 IP address (0 hosts up) scanned in 3.03 seconds

Then, with -pn
>> nmap 35.239.221.133 -Pn

>>Starting Nmap 6.40 ( http://nmap.org ) at 2019-04-23 21:23 UTC

>>Nmap scan report for 133.221.239.35.bc.googleusercontent.com (35.239.221.133)

>>Host is up (0.00092s latency).

>>Not shown: 998 filtered ports

>>PORT     STATE  SERVICE

>>22/tcp   open   ssh

>>3389/tcp closed ms-wbt-server

>>Nmap done: 1 IP address (1 host up) scanned in 4.45 seconds

That's how I realized that the firewall rule I set up for the honeypots was not applied to the honeypot VMs. I corrected that and the probe worked. I also started to have attacks coming in from the outside.



## Summary of the data collected: number of attacks, number of malware samples, etc.
## Any unresolved questions raised by the data collected
