---
description: Some suggestions of common ports to secure and why
---

# Ports

## What is a port and why is it important?

Ports, specifically computer port protocols allow computers to easily differentiate between different kinds of **traffic**

For example, emails go to a different port than webpages, for instance, even though both reach a computer over the same Internet connection.

There is a lot of different types of services and each port is special in its own characteristic into what it is used for and how it allows allows the type of traffic to go through.



## Ports

| Port Number | Service            | Protocol |
| ----------- | ------------------ | -------- |
| 20-21       | FTP                | TCP      |
| 22          | SSH                | TCP      |
| 23          | Telnet             |          |
| 25          | SMTP               |          |
| 53          | DNS                | TCP/UDP  |
| 123         | NTP                | UDP      |
| 110         | POP3               |          |
|             |                    |          |
| 445         | SMB/Cifs           |          |
| 500         | SIP                | UDP      |
| 993         | IMAPS              | TCP      |
| 3389        | RDP                | TCP      |
| 8080        | Web Server Traffic |          |

Common Ports 1 to 1,023.

Registered Ports 1,024 to 49,151.&#x20;

Dynamic and/or private ports 49,152 to 65535



## Vulnerabilities

Vulnerabilities, the not so good stuff...

There are many reasons why it is important to know about ports and the flow of traffic how it goes from one place to another. With this information you can picture different designs to allows specific types of functionalities and systems to work depending on your setup.

### DDoS Attacks

DDoS attacks are popular attack as they are highly successfully and low-cost to execute.

Basically the goal for DDoS attacks are to exhaust a defender's resources, resulting in a shutdown of services.

In order to prevent this type of attack, firewall discards all packets that use the TCP protocol and is fragmented. Incoming TCP packets are only allowed via **Dynamic Packet Filters.**

DDoS attacks cannot be prevented by simply increasing the network bandwidth.

There are many different types of the DDoS attack such as multi-layered DDoS. Some ideas of prevent / reducing the likelihood of an attack.

1. Inspect / detection of the increase of traffic.
2. Avoid become a bot slave to the DDoS botnet.
3. Filtering specific traffic and blocking malicious IP addresses.
4. Reduce Attack Surface Exposure.
5. Black Hole Routing to drop traffic.
6. Rate limiting
7. Geo-access limiting

These are few starter points in which you can put in preventive measures in place when you have your system.&#x20;

#### Rate Limiting

Rate limiting can be found wihtin the Firewall > Traffic Shaper > Limiters

{% hint style="info" %}
Change the bandwidth number depending on your allocated internet allowance.
{% endhint %}

![](<../.gitbook/assets/image (21).png>)

Lan Upload limiter

![](<../.gitbook/assets/image (22).png>)

I left the mask at none (meaning all) , no other settings set and save.

* **Mask**: this parameter allows to define how the limitation will be applied to the traffic. 3 choices are available:
  * none: the limitation will apply to all traffic as a single set. In our case, this is what we choose (we want the whole outgoing traffic to be limited to 50 Mbps).
  * Source addresses: the limitation will apply per source IP address (or group of source IP addresses, depending on the mask). So, to perform a limitation by IP address of a network, we choose “Source addresses” and specify a /32 mask. This is the value we will choose when we will configure the queue of our Upload pipe.
  * Destination addresses: the limitation will apply by destination IP address (or group of destination IP addresses, depending on the mask). This is the value we will choose when we will configure the queue of our Download pipe.

Download limiter

This is very similar to the upload limiter. The only difference is that we chose the mask as destination addresses.

![](<../.gitbook/assets/image (23).png>)&#x20;

After when fully save is to apply them to the firewall.



Go into the specific rule you are looking to limit.

File > Rules

Go into the specific rule setting and display advanced.

![](<../.gitbook/assets/image (24).png>)

Near the bottom of the page is the options you can input in the dropdown menus:

![](<../.gitbook/assets/image (25).png>)

To check that this is working you can look at the Diagnostics > Limiter Info.

Each pipe and is presented in text format with the parameters and values set.

