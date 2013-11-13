---
layout: post
title: Setting up a SVN repository and working copy
categories:
- Waffle
tags: []
status: publish
type: post
published: true
meta:
  _edit_last: '1'
---
I have just started to use subversion for version control. It's been pretty problematic to start with but I think I have cracked it now. I haven't read the manual properly, I just dipped in now and then when I needed to. So here for future reference is how to create a repository and working copy.<br /><br /><ol><li>shh in to the server with SVN on it.</li><li>go to the directory where SVN resides in my case /mnt/bigdisk/subversion.</li><li>use the command svnadmin create project_name, so that I know that this is a repository I always name the directory like this svn_projectname.</li><li>once you have the repository set up you need to do a SVN import like this; svn import path/to/project/files file:///repository_name/project -m "First Import".</li><li>You will now see the terminal spin whilst importing all of the files.</li><li>Then go to you SVN client and do a SVN checkout.</li><li>you now have a working copy to play with change files and add them when you have a fixed bit of the site.</li></ol>Note: I'm not using branches trunk and tags in simple things like this as there aren't likley to be many branches to a small sites.<br /><br /><br /><p class="poweredbyperformancing">Powered by <a href="http://scribefire.com/">ScribeFire</a>.</p>
