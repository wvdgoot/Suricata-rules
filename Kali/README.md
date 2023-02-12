# Kali

This directory contains rules written for the detection of a Kali Linux machine
on the network.

## Kali Linux host

### DHCP connection with hostname `kali`
If the hostname of the Kali machine was not changed by the user, the default is
`kali`. When a Kali machine is booted, it will send a DHCP request to get an IP
address and in this DHCP request you can see the hostname.

## Kali Linux repository connection

The `kali-repository.rules` file consists of rules that detect a connection to
the Kali Linux repositories, based on the domain names. There are different types 
of packets of which we can use the metadata to notice a connection to the repo
domains.

TODO: automate domain name checker with script.

### HTTP `Host` header
TODO

### TLS Server Name Indication
The SNI field in a TLS packet contains the domain that the HTTP(S) packet goes to.

### DNS query
TODO
