---
title:  "Hostinger"
layout: post
categories: 
  - notes
permalink: /notes/2025-02-04-hostinger
last_modified_at: 2025-02-04
---

Originally, I was using DigitalOcean and mostly running Ubuntu for my proxy OS needs. Later, I discovered that Hostinger (hostinger.com) offers similar functionalities—but with Kali Linux as the operating system—so I decided to give it a try.   

You can use my code to get a 20% discount:  
https://hostinger.com?REFERRALCODE=NMDOOOLAN1G6  

During the process, while installing the Go lang tool, I encountered the following error:  

```
dial tcp: lookup proxy.golang.org on [::1]:53: read udp [::1]:46622->[::1]:53: read: connection refused
```

To fix the issue, we can use:  

```
ln -sf /run/systemd/resolve/stub-resolv.conf /etc/resolv.conf  
```
And then I added `nameserver 8.8.8.8` to `/etc/resolv.conf`.  
