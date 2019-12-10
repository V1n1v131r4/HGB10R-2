# HGB10R-2
Exploit Modem Humax HGB10R-2

This is a Proof of Concept on how to get the Humax HGB10R-2 router admin credentials when sniffing the HTTP traffic packets.

In Brazil this router is available from ISP NET and is present in most homes.

Using Wireshark for packet capture and a Firefox browser to access the router management panel, it was possible to realize that admin credentials were passed using Basic Authentication (Base64-encoded only), as shown in the images below:

![Kali](http://ciber.sejalivre.org/HGB10R-2/kali.png)

Another vulnerability (which has been around since the HG100 2.0.6 release as per CVE-2017-7317) is that an attacker could gain router admin credentials and Wi-Fi credential by having access to backup file as per images below:
