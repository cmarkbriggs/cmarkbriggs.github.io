---
layout: post
title: Sysloggin' at Home
tags: technology networking
---

A couple of years ago, I replaced my Netgear "gaming" wireless router at home with a Ubiquiti Unifi setup. Although the Netgear router worked fairly well, it didn't provide me the level of customization I wanted in my networking setup. The impetus was installing quite a few smart home devices and my desire to isolate these IoT devices from the user network.

I purchased a Unifi Secure Gateway, two Unifi managed switches, and a Unifi wireless access point. Coming from a work background that has included a lot of enterprise networking, setting up the Unifi devices was really straightforward. I would venture to say that anyone who is fairly technical but with only a rudimentary background in networking could still set up a Ubiquiti network fairly easily.

I set up two VLANs, one for user devices such as computers, iPhones, and iPads, and a second VLAN for the smart home devices. I then configured a firewall rule that allows the IoT VLAN to communicate with the internet but not the user VLAN. Due to the nature of IoT devices and their infrequent updates, this gives me some peace of mind about my user devices, since if an IoT device were to be hacked, the user devices on the other VLAN could not be reached.

Last weekend, I finally got around to do something I've been meaning to do for quite a while - set up a syslog server on my home Windows server. I installed the free version of Kiwi Syslog Server. Since the free version allows for five input sources, and I only have four network devices, this version is all I need. After configuring Kiwi and then setting the IP address of the server in the Unifi configuration, I could immediately see syslog messages appearing in Kiwi.

I also set up Kiwi to send me emails if the number of email messages in an hour reaches a certain threshold. I've received a few of these emails of the past week, but as you can see here, there aren't any critical errors I need to worry about.

<p align="center"> 
  <img src="/images/Syslog_Messages_001.png">
</p>

Was having a syslog server for my home network really necessary? No, not at all. However, as a technology enthusiast with a substantial home network setup, I like the insight such an implementation provides me.
