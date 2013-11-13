---
layout: post
title: Restarting the Local DNS server
categories:
- Waffle
tags: []
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
Heres a quick note on how to restart the local DNS server.

1. ssh in to the server
2. at the $ prompt type "sudo /etc/init.d/named restart"
3. all done

Thats it simple as that you need know no more apart from the fact that you obviously have all of the usual attributes stop and start. Okay thats how to do it on linux but on Mac OS X you will want to do the following;

- open the terminal
- at the $ type "sudo lookupd -flushcache"
- all done
