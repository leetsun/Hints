# Info Leak in Linksys-WRT54GL Router

## Overview

    * Type: Information leak
    * Supplier: Linksys
    * Victim URL: http://192.168.1.1/SysInfo1.htm
    * Product: WRT54GL Wireless-G WiFi Router
    * Affect version: (lastest) v4.30.18
    * Firmware download: https://downloads.linksys.com/downloads/firmware/FW_WRT54GL_4.30.18.006_US_20160108.bin
 

## Description

An infomation leaking vulnerability is at the web management interface of the affected routers. Without any permition, attacker can get sensitive information such as ram size, mac address from the victim URL.

The victime url is a hidden interface and isn't been protected by authentication.

## Business Impact

The leaked information is sensitive and could result in serious damage. Thus the vulnerability is very dangerous which could also result in reputational damage for the business through the impact on customers' trust.

## Steps to Reproduce

Visit the victime URL from the web, such sensitive information as ram size, mac address and some configurations are explosed as below:
'''
language=EN;
Flash Type=;
CPU Clock=;
sdram_init=;
sdram_config=;
sdram_ncdl=;
pa0b0=;
pa0b1=;
pa0b2=;
Write Mac Address=01:23:45:67:89:ab;

get wl_gmode=1;

totalram=258420736, freeram=241950720, bufferram=241664;
uptime=2160;

eou_configured=0;
get_eou_index=0;
get_sn_index=0;
get_sn=;

get_mac_index=0;
get_mac=;
ses_status=;
ses_count=0;

'''
