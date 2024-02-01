# Info Leak in Netgear-R7000 Router

## Overview

    * Type: Information leak
    * Supplier: Netgear (https://www.netgear.com/)
    * Victim URL: http://192.168.1.1/debuginfo.htm
    * Product: R7000 —  Nighthawk AC1900 Smart WiFi Dual Band Gigabit Router
    * Affect version: (lastest) V1.0.11.136_10.2.120
    * Firmware download: https://www.downloads.netgear.com/files/GDC/R7000/R7000-V1.0.11.136_10.2.120.zip?_ga=2.104770566.764029436.1681304815-1560383626.1681304810
 

## Description

An infomation leaking vulnerability is at the web management interface of the affected routers. Without any permition, attacker can get sensitive information from the victim URL.

The victime url is a hidden interface and isn't been protected by authentication.

## Business Impact

The leaked information is sensitive and could result in serious damage. Thus the vulnerability is very dangerous which could also result in reputational damage for the business through the impact on customers' trust.

## Steps to Reproduce

Visit the victime URL from the web, sensitive information is explosed as below:
'''
WAN connection type: DHCP
Product model name: R7000
'''
