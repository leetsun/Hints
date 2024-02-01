# Info Leak in Linksys-WRT54GL Router

## Overview

    * Type: Information leak
    * Supplier: Linksys
    * Victim URL: http://192.168.1.1/wlaninfo.htm
    * Product: WRT54GL Wireless-G WiFi Router
    * Affect version: (lastest) v4.30.18
    * Firmware download: https://downloads.linksys.com/downloads/firmware/FW_WRT54GL_4.30.18.006_US_20160108.bin
 

## Description

An infomation leaking vulnerability is at the web management interface of the affected routers. Without any permition, attacker can get sensitive information such as 'NetworkMode', 'channel' from the victim URL.

The victime url is a hidden interface and isn't been protected by authentication.

## Business Impact

The leaked information is sensitive and could result in serious damage. Thus the vulnerability is very dangerous which could also result in reputational damage for the business through the impact on customers' trust.

## Steps to Reproduce

Visit the victime URL from the web, such sensitive information as 'NetworkMode', 'channel' and some configurations are explosed as below:
'''
RouterName:WRT54GL
11gNetworkMode:Mixed
11gSSID:linksys
11gChannel:6
11gSSIDBroadcast:Enabled
SecurityMode:Disable
Encryption:off
ses_status:
ses_count:0
'''
