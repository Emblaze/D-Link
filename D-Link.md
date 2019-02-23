# D-Link Level 2 Support Technician Handbook

<!-- TOC depthFrom:1 depthTo:3 withLinks:1 updateOnSave:1 orderedList:0 -->

- [D-Link Level 2 Support Technician Handbook](#d-link-level-2-support-technician-handbook)
	- [Compatibility List](#compatibility-list)
	- [Knowledge Base](#knowledge-base)
	- [Technical Support Contact details](#technical-support-contact-details)
	- [Networking Fundamentals](#networking-fundamentals)
	- [Customer links of interest](#customer-links-of-interest)
	- [Main product families](#main-product-families)
		- [Switches](#switches)
		- [Access Point Controllers](#access-point-controllers)
		- [Access Points](#access-points)
	- [Product Configuration Basics](#product-configuration-basics)
	- [FAQ](#faq)

<!-- /TOC -->

## Compatibility List



## Knowledge Base



## Technical Support Contact details

Monday to Friday, 9:00 am - 7:00 pm (except bank holidays)

#### Phone

| Country | Phone number      |
| ------- | ----------------- |
| France  | +33 1 76 54 84 17 |
| Italy   | +39               |
| UK      | +44               |

#### Self-service Portal

[Registered Customer](http://services.eu.dlink.com/home/main/SSPLogin.aspx?jdecloselink=http%3A%2F%2Fwww.dlink.com%2Ffr%2Ffr%2Fsupport%2Fproduct-registration-and-support-log-in&language=F) | [New customer](http://services.eu.dlink.com/home/main/CustomerRegister.aspx?jdecloselink=http%3A%2F%2Fwww.dlink.com%2Ffr%2Ffr%2Fsupport%2Fproduct-registration-and-support-log-in&language=F)

#### [Chat](https://www.livechatinc.com/?partner=lc_4932971&utm_source=chat_button)



## Networking Fundamentals

![IPv4 Address](media/300px-Ipv4_address.svg.png)

| Device type   | Connectivity | Services                | Notes                     |
| ------------- | ------------ | ----------------------- | ------------------------- |
| Modem Routers | ISP/LAN/WAN  | DHCP/DNS/NAT            |                           |
| Routers       | LAN to LAN   | Manual configuration    | No extra NAT level/subnet |
|               | LAN to WAN   | Automatic configuration | Extra NAT level/subnet    |
|               |              |                         |                           |

## Customer links of interest

*   [EU Website](https://eu.dlink.com/fr/fr)
*   [FTP site](ftp://ftp.dlink.eu/)
*   [DLink Network Assistant (DNA)](ftp://ftp.dlink.eu/Products/dna/dna/driver_software/DNA_sw_4-0-0-8_eu_en_20180307.zip)
*   [DNA Chrome extension](https://chrome.google.com/webstore/detail/d-link-network-assistant/eoenegoacckkpkijhfhijfechhhpkbmp?hl=en)
*   [mydlink](https://www.mydlink.com/download)
*   [mydlink app](https://www.mydlink.com/apps)

DNA uses **SNMP** to discover hardware & IP's.

## Main product families

### Switches

| Switches | Default IP  | Notes      |
| -------- | ----------- | ---------- |
| DWS      | 10.90.90.90 | Manageable |
| DGS      | 10.90.90.90 |            |
| DES      | 10.90.90.90 |            |
| DXS      | 10.90.90.90 | Stacking   |

### Access Point Controllers

| Access Point Controllers | Access Points | Default IP   | Notes                            |
| ------------------------ | ------------- | ------------ | -------------------------------- |
| DWS (Manageable)         |               |              |                                  |
| DWC                      | DAP*          | 192.168.10.1 | Computer must on the same subnet |
| Nuclias                  | DBA*          | [nuclias.com](https://www.nuclias.com)  | SaaS                             |
\*Some DAP/DBA cannot be managed.

### Access Points

| Access Points | Default IP   | Notes              |
| ------------- | ------------ | ------------------ |
| DAP           | 192.168.0.50 | Manageable via CWM |
| DBA           | nuclias.com  |                    |
| DWL           | 10.90.90.91  | Manageable via DWC |

| Cameras | Default IP   |
| ------- | ------------ |
| DCS     | 192.168.0.20 |

## Product Configuration Basics

 Some product features/capacity require addtional licence(s):exclamation:

*   ### DWC 1000/2000 Access Point Controllers

    Allows control of DWL AP series.

1.  Make sure the laptop/desktop and AP controller ar on the same subnet/network segment

2.  Setup LAN settings and enable DHCP

| Setting  | Default       |
| -------- | ------------- |
| IP       | 192.168.10.1  |
| Mask     | 255.255.255.0 |
| Usermane | admin         |
| Password | admin         |

*   ### DSR 250(N)/500(N)/1000(N) Series Routers


## FAQ

*   ### Stacking

    1.  Which model(s) of switches?

    2.  Which type of SFP´s/Mini GBIC?

    3.  What type of fiber is used?

    4.  What is the length of the cable between the switches?
