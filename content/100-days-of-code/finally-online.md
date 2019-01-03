---
title: "Finally Online"
date: 2019-01-03T02:36:37-05:00
draft: false
tags: 
  - hugo
  - Kemo Networks
  - nginx
  - letsencrypt
---

Fucking did it.  That was a lot harder than it had to be, though mostly by my own fault for trying to skip through this shit really quickly.

So the idea was to get this site that you're reading now, a Day 2 of 100DOC project, online at it's home and also to set up the syncing.  It's a static website, how hard could that be?

## Day 2
### Project: Kemo Networks (this site)
#### Task: Get things online and syncing

- This is a static website, I thought yay, no PHP or MariaDB to deal with, throw up a server and boom, easy.
- EVIDENTLY Hugo versions are widely different so while I tried to stuff this into a corner of an older Ubuntu 16 LTS box, the version of Hugo was too old to build this site so I decided to get this its very own VPS.  Comfy.
- Got it rolling, installed Fedora and spent a few hours battling permission issues that I thought were SELinux's fault but even with it disabled it persisted.  Reinstalled with Ubuntu 18 LTS, same thing.
- Funny thing, I try to run all SSL - it's free and easy, no reason not to.  Well, evidently Hugo hard-codes the entire URI path so while my config.toml file had https://kemo.network in there, the assets wouldn't load and I hadn't set up SSL yet because I just wanted to test it working...
- So proper order of operations would have been install nginx then do SSL installation, then run Hugo...
- Got SSH secure, Fail2Ban, a few other goodies to keep things secure rolling on this new node, loaded nginx and setup the site config
- Installed Letencrypt, failed verification because I forgot about the **www** records and fucking IPv6 AAAA records that I had previously set...so waiting game
- Installed Go and compiled Hugo from source since the distro version was older than I needed.
- Git clone, hugo, test, boom, yay!  Things work!
- Synced up the Git repo with some sweet crontab "git pull" Continuous Delivery goodness (ha)
- Synced up content files via Google Drive folder and FUSE

So now I have this site hosted and synced via GitHub, and the larger images being synced via a Google Drive folder and this project: https://web.archive.org/web/20180826162814/http://xmodulo.com/mount-google-drive-linux.html

It only took me all fucking night long, but I wanted to do it come hell or high water.
