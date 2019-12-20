# HGB10R-2
Exploiting Router Humax Wireless Voice Gateway HGB10R-2

On this PoC i published the CVEs below:

CVE-2019-19889: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-19889
CVE-2019-19890: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-19890


## Admin Credentials on HTTP Request

This is a Proof of Concept on how to get the Humax HGB10R-2 router admin credentials when sniffing the HTTP traffic packets.

In Brazil this router is available from ISP NET and is present in most homes.

Using Wireshark for packet capture and a Firefox browser to access the router management panel, it was possible to realize that admin credentials were passed using Basic Authentication (Base64-encoded only), as shown in the images below:

![Kali](http://ciber.sejalivre.org/HGB10R-2/kali.png)

![HGB10R-2](http://ciber.sejalivre.org/HGB10R-2/hgb10r_2.png)

![Wireshark](http://ciber.sejalivre.org/HGB10R-2/wireshark.png)


### PoC on Video:

[![HGB10R-2](https://i.ibb.co/9r0DCFK/https-i-vimeocdn-com-video-838301175-720.jpg)](https://vimeo.com/378517982 "HGB10R-2")


## Admin Credentials on Backup File

Another vulnerability (which has been around since the HG100 2.0.6 release as per CVE-2017-7317) is that an attacker could gain router admin credentials and Wi-Fi credential by having access to backup file as per images below:

![Admin on bkp file](http://ciber.sejalivre.org/HGB10R-2/admin_pass.png)

![Base64](http://ciber.sejalivre.org/HGB10R-2/base64.png)

![Wi-Fi Pass](http://ciber.sejalivre.org/HGB10R-2/wifi.png)
