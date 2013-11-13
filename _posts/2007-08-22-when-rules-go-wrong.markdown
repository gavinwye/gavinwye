---
layout: post
title: When rules go wrong
categories:
- Waffle
tags: []
status: publish
type: post
published: true
meta:
  _edit_last: '1'
  dsq_thread_id: ''
---

I use Apple's Mail.app which is fine it is integrated nicely in to my work flow, It links to <a title="Daylight" href="http://marketcircle.com/daylite/index.html" target="_blank">Daylight</a> via DMI and most of the time it just works. However I get a lot of mail and I've been getting more and more busy lately so I have stopped checking the not important stuff. The sort of stuff that I don't want to junk but don't want to read now.

So I created a rule quickly (which is where everything went wrong) to put everything from the people whose mail I hadn't read in the last month in a folder called NQJBNTI (Not Quite Junk But Not That Important). I did it just before <a title="Business Bricks" href="http://upcoming.yahoo.com/event/215585/" target="_blank">Business Bricks</a> on Friday and then someone came in so I didn't finish the task properly. I just shut my laptop and forgot about it.

Because I had forgotten about the rule and not checked my mail for the rest of Friday or the weekend by the time it got to Monday and I checked my mail and didn't get some mails from people who had sent them to me I immediately thought it must have been a problem with the mail server.

I spoke to <a title="Symon" href="http://homepage.mac.com/symonc/" target="_blank">Symon</a> and he told me to telnet in to the mail server so that I could see if there was mail there (this is apparently the same protocol as mail.app uses) so that proves that mail is working. I installed Packet Peeper to sniff the packets and everything is working fine. I created a new mail account and could receive mail on that account. So the server is working and so is mail.app. Then Dave said the only thing left is a problem with rules but I can't see that being a problem! Rules I did something in there on Friday! I checked and the rule was set to exclude all mail from my in box unless it was from one person. Doh!

So the moral of the story is check the simple stuff first, and try and remember what you did yesterday!

Anyway the real point of this post is here's how to telnet in to a mail server which I found really cool. I love stuff like this and here's a record for when I forget.

Open the terminal
at the prompt ($) type telnet mailservername 110
you should get a message back like Ok hello there
type the following
USER username
It will then ask for the password for the account type:
PASS password
you should then get a logged in message
type list
you will then see a list of all the mail on the serve to read the mail type
retr 1 (where 1 is the number of the mail)
to quit type quit
