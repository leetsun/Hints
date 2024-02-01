# Configure service in Motorola-CX2L Router without permission

## Overview

    * Type: hidden interface
    * Supplier: Motorola
    * Product: CX2L, firmware version 1.0.1
    * Affect version: 1.0.1

## Description of the Vulnerability

A hidden interface exists in motorola router CX2L that allows opening/closing 'telnet' service without any permission. The vulnerability is easily exploited, just sending a request to the device remotely. 

## Steps to Reproduce

I have put the PoC (exp.py) in the below link. Configure the target ('device_web_ip' in exp.py), then execute the exp, the 'telnetd' service is activated. You can telnet the router to check.

poc link: xxx