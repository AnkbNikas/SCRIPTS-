#!/usr/bin/python3

import nmap

print("[Info] Open ports scan tool in an IP address")
print(" || In Python using Nmap")

host= input("[+] Set your target Host: ")
nm= nmap.PortScanner()
open_ports="-p"
count=0
results= nm.scan(hosts=host, arguments="-sT -n -Pn -T4")
#print (results)
print("\nHost : %s" % host)
print("State : %s" % nm[host].state())
for proto in nm[host].all_protocols():
    print("Protocol : %s" % proto)
    print()
    lport = nm[host][proto].keys()
    sorted(lport)
    for port in lport:
        print ("port : %s\tstate : %s" % (port, nm[host][proto][port]["state"]))
        if count==0:
            open_ports= open_ports+" "+str(port)
            count=1
        else:
            open_ports= open_ports=","+str(port)
print("\nopen_ports:"+open_ports+" "+ str(host))
