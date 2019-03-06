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

## Technical Support Contact Details

Monday to Friday, 9:00 am - 7:00 pm (except bank holidays)

### Phone

| Country  | Phone number      |
| -------- | ----------------- |
| France   | +33 1 76 54 84 17 |
| Italy    | +39               |
| Spain    | +34               |
| Portugal | +351              |
| UK       | +44 843 508 6179  |

### D-Link Knowledge Base

[D-Link Knowledge Base](http://dse-kb.dlink.it/index.php)

### Self-service Portal [services.eu.dlink.com](http://services.eu.dlink.com)

[Registered Customer](http://services.eu.dlink.com/home/main/SSPLogin.aspx?jdecloselink=http%3A%2F%2Fwww.dlink.com%2Ffr%2Ffr%2Fsupport%2Fproduct-registration-and-support-log-in&language=F) | [New customer](http://services.eu.dlink.com/home/main/CustomerRegister.aspx?jdecloselink=http%3A%2F%2Fwww.dlink.com%2Ffr%2Ffr%2Fsupport%2Fproduct-registration-and-support-log-in&language=F)

### [Chat](https://www.livechatinc.com/?partner=lc_4932971&utm_source=chat_button)

## Customer links of interest

*   [EU Website](https://eu.dlink.com/fr/fr)
*   [EU FTP site](ftp://ftp.dlink.eu/)
*   [DLink Network Assistant (DNA)](ftp://ftp.dlink.eu/Products/dna/dna/driver_software/DNA_sw_4-0-0-8_eu_en_20180307.zip)
*   [DNA Chrome extension](https://chrome.google.com/webstore/detail/d-link-network-assistant/eoenegoacckkpkijhfhijfechhhpkbmp?hl=en)
*   [mydlink](https://www.mydlink.com/download)
*   [mydlink app](https://www.mydlink.com/apps)
DNA uses **SNMP** to discover hardware & IP's.

## Networking Fundamentals

![IPv4 Address](media/300px-Ipv4_address.svg.png)/ Notion of IP Classes

| Device type   | Connectivity | Services                | Notes                     |
| ------------- | ------------ | ----------------------- | ------------------------- |
| Modem Routers | ISP/LAN/WAN  | DHCP/DNS/NAT            | -                         |
| Routers       | LAN to LAN   | Manual configuration    | No extra NAT level/subnet |
|               | LAN to WAN   | Automatic configuration | Extra NAT level/subnet    |

## Product Configuration Basics

Some product features/capacity require addtional for-pay licence(s).

### DWR Routers

| Model   | Features |
| ------- | -------- |
| DWR‑921 | 4G/LTE   |

DSL routers are handled by Level 1 Tech Support.

### DSR 250N/500N/1000N Series Routers

| Model      | Users | Current Rev. | Notes |
| ---------- | ----- | ------------ | ----- |
| DSR-250N   | 10    | B            |       |
| DSR-500N   | 25    |              | EOL   |
| DSR-1000N  | 50    |              | EOL   |
| DSR-1000AC | 50    | A            |       |

### DES/DGS/DXS Switches

Generally deployed in conjonction with a router (upstream), an AP controller (and AP´s).
No DHCP server included, uses broadcast domain (aka "APIPA") address by default.

| Switches | Default IP  | Notes      |
| -------- | ----------- | ---------- |
| DGS      | 10.90.90.90 |            |
| DES      | 10.90.90.90 |            |
| DXS      | 10.90.90.90 | Stacking   |

*   Related Wikipedia Links
[VLAN](https://en.wikipedia.org/wiki/Virtual_LAN)
[VLAN Tagging (IEEE 802.1Q)](https://en.wikipedia.org/wiki/IEEE_802.1Q)
[Link aggregation/Trunking](https://en.wikipedia.org/wiki/Link_aggregation)
[Quality of Service](https://en.wikipedia.org/wiki/Quality_of_service)

#### VLAN´s Setup (LAN to LAN)

 VLAN modes: **Access** only, **General** and **Trunk (recommended)**.

 VLAN ports can be either **Tagged** (to allow Router-level defined VLAN´s to be deployed at switch level, QoS, Firewall, VPN), **Untagged** (for client/management) and **Not member**.

 **Caveats**:

*   For firmware upgrades, ensure it´s downloaded from the right country website **&** that it matches the product revision.
*   If a manageable switch has no management VLAN, define VLAN1 port to allow management.
*   Captive portals can only be setup at default VLAN1 level.
*   VPN IPSec ???

#### DWC 1000/2000 Access Point Controllers

Allows control of DWL AP series.
1.  Make sure the laptop/desktop and AP controller ar on the same subnet/network segment
2.  Setup LAN settings and enable DHCP

| Setting  | Default       |
| -------- | ------------- |
| IP       | 192.168.10.1  |
| Mask     | 255.255.255.0 |
| Usermane | admin         |
| Password | admin         |

### Access Point Controllers

| Access Point Controllers | Access Points | Default IP                             | Notes                               |
| ------------------------ | ------------- | -------------------------------------- | ----------------------------------- |
| DWS (Manageable)         |               |                                        |                                     |
| DWC                      | DAP*          | 192.168.10.1                           | Computer must be on the same subnet |
| Nuclias                  | DBA*          | [nuclias.com](https://www.nuclias.com) | SaaS                                |

\*Some DAP/DBA cannot be managed.

*   Check and Adjust DHCP server settings.
*   Configure VLAN´s
*   Create and deploy profiles

Caveat: Pushing configuration changes in production disconnects users.

### Access Points

Recommended max. # of AP´s: 34

Mind the PoE power/Watts budget

Tip: Save configuration changes often to avoid reconfiguration after short timeout

*   **Multi-SSID** (Primary, S1, S2, ..., Sn)

*   **Port VLAN´s ID´s** (PVID) must **match** router-level defined VLAN ID´s. Enabling AUTO is recommended.

*   **Modify** AP´s IP address, save configuration and test it from a client.

| Access Points | Default IP   | Notes              |
| ------------- | ------------ | ------------------ |
| :	DAP:        | 192.168.0.50 | Manageable via CWM |
| :	DBA:        | nuclias.com  |                    |
| :	DWL:        | 10.90.90.91  | Manageable via DWC |

#### Access Point Modes

##### Access Point Mode

Access Point mode is used to connect to wireless clients(wireless adapter cards) such as laptops, desktops, and PDAs. Wireless clients can only communicate to AP's in Access Point mode.

##### Access Point Client / Wireless Client Mode

AP Client or Wireless Client mode allows the Access Point to become a wireless client to another AP. In essence the AP has now become a wireless adapter card. You would use this mode to allow an AP to communicate with another AP.

Note: Not all Access Points support AP Client mode. If the mode is supported it will operate only with devices of the same series. Wireless cards will not communicate with access points in AP Client/ Wireless Client mode.

##### Point-to-Point / Wireless Bridge

Point-to-Point / Wireless Bridge mode allows the Access Point to communicate with another Access Point capable of point-to-point bridging. However, be aware that most manufacturers use proprietary settings when enabling bridging mode in the Access Point. A typical scenario for this selection is connecting two buildings through a wireless connection.

Note: Not all Access Points support Point-to-Point / Wireless Bridging mode. If the mode is supported it will operate only with devices of the same series. Example: the DWL-900AP will communicate with another DWL-900AP, and the DWL-900AP will communicate with another DWL-900AP. The DWL-900AP will not communicate with aDWL-900AP in this mode. Wireless clients will not communicate to AP's in this mode.

##### Point-to-Multipoint / Multi-point Bridge

Point-to-Multi-point / Multi-point Bridge mode is the same as Point-to-point / Wireless Bridge mode, however, this mode allows you to use more than two Access Points.

Note: Not all Access Points support Point-to-Multipoint / Wireless Bridging mode. If the mode is supported it will operate only with devices of the same series. Example: the DWL-900AP will communicate with another DWL-900AP, and the DWL-900AP will communicate with another DWL-900AP. The DWL-900AP will not communicate with a DWL-900AP in this mode. Wireless clients will not communicate to AP's in this mode.

##### Repeater Mode

As a Wireless Repeater, the Access Point extends the range of the wireless network by repeating the wireless signal of the remote AP (Access Point). The Ethernet MAC address of the remote AP is required for the Access Point to act as a wireless range extender.

Note: Not all Access Points support Repeater mode. If the mode is supported it will operate only with devices of the same series. Example: the DWL-1000AP will communicate with another DWL-1000AP, and the DWL-900AP will communicate with another DWL-900AP. TheDWL-1000AP will not communicate with a DWL-900AP in this mode. Wireless clients will communicate to APs in this mode.

##### WDS Mode

The Wireless Distribution System (WDS) mode is similar to the Bridge mode. In WDS mode you can get your Access Points to communicate with each other wirelessly. Note that in this mode the access points will not communicate with wireless clients.

##### WDS with AP Mode

This mode allows your Access Points to communicate with each other wirelessly and at the same time allows wireless clients to connect to the network.

### Cameras

Several configuration options: via the Setup Wizard (Windows/Mac) or manually via the web interface (with a system on the same subnet).



| Cameras | Default IP   |
| ------- | ------------ |
| :DCS:   | 192.168.0.20 |

## FAQ

*   ### Stacking

    1.  Which model(s) of switches?

    2.  Which type of SFP´s/Mini GBIC?

    3.  What type of fiber is used?

    4.  What is the length of the cable between the switches?

## Processes

### JDE E1, Cases and RMA's Management

**[JDE login](https://pd812.erp.dlink.eu/jde/E1Menu.maf) > Customer Service Management > Case Management**

**Caveat:** JDE times out after 10 to 20 min. Save your work regurlarly!

| Customer   | Case Management Section  | Code in report |
| ---------- | ------------------------ | -------------- |
| Without SN | Case <country> L2 w/o SN | :CL:           |
| With SN    | Case <country> L2        | :CN:           |

**Case Inquiry View Layout & Format**

| Case History     | Internal TS History | Email Drafting |
| ---------------- | ------------------- | -------------- |
| Paste last Email | Follow below format | Use templates! |

**Internal Troubleshooting History Format**

DATE:

AGENT:

REASON OF CALL:

-

CUSTOMER TEST: None

SOLUTION:

**Case Creation**

JDE > Case Management SE > Case SE L2 > Add

| Required Info           |
| ----------------------- |
| S/N                     |
| First and last name     |
| Company/organisation    |
| Phone and Email         |
| Fill in the 3 dropdowns |

**JDE Status Rules**

| JDE | Status Rules |
| --- | ------------ |
| 100 | Unassigned / New. This is an automatic status while creating a new case.. New SS case created will use automatically the status 100. These cases must be managed as soon as possible (ref. D‐Link – MST agreement) |
| 105 | Escalated. To be used when escalate a case to an upper level. (2nd, 3rd or RMA) |
| 110 | Open / Active. Use this status when opening a case. At the end of the call, the status of the case must be changed to 130, 200, 210, 105 or 999. |
| 120 | Reopen / Review. This status can be used only for re‐open a complete case (999) (Otherwise you’ll receive an error message). |
| 130 | Research. Use this status when further information are needed therefore you are planning a callback to customer. Do not leave the cases in that state for more than 10 days. |
| 200 | Waiting for Customer. Use this status when customer have to provide some info related the issue (driver version, Fw version, etc). Do not leave the cases in that state for more than 10 days. |
| 210 | Waiting for POP. Use this status when customer have to provide a Proof of Purchase or the picture of the label of the Serial Number. Do not leave the cases in that state for more than 10 days. |
| 995 | Spam – Cancelled. Use this status when you receive a spam. |
| 997 | Cancelled. Use this status to close duplicate case |
| 999 | Complete. Use this status when a case is solved or when you provide to customer a solution. |

**JDE Presales Rules**

| JDE Presales rules                       |
| ---------------------------------------- |
| Must be a CN case (no serial available)  |
| Description of the case must be PRESALES |
| Failure code must be: ‘C1’               |
| Analysis code must be: ‘C2’              |
| Resolution must be: ‘N4’                 |

## Phone/ACD System

To place an outbound call, use 3 then country code + line number

| Queue        | ACD  |
| ------------ | ---- |
| FR Consumer  | 5074 |
| FR RMA       | 5078 |
| FR Business  | 5075 |
| FR Tech A    | 5083 |
| FR Resellers | 5076 |
