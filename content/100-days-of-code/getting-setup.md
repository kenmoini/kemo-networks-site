---
title: "Getting Setup"
date: 2019-01-01T19:16:35-05:00
draft: false
tags: 
  - hugo
  - static site generators
  - kemo networks
---

Alright, this isn't too bad, I like the digs and I can get behind the idea.
So this whole Static Site Generator thing is sort of new to me...I've used Hugo before in passing in a collaborative project but you know me, I love me some PHP and WordPress and Laravel and all that other fun stuff.

That fun stuff though has a tendancy to get hacked and I had no inclination to manage another internet property so I decided to dive into Hugo for one of my own personal projects...which is what you're reading right now...

This will start the chronicalling of my various not-so-serious and holy-shit-balls-cool adventures.  This one in particular being this so called "100 Days of Code" or #100DaysOfCode.

What will I be coding?  I have no fucking idea specifically, probably a couple different projects as I've got a stack of them...I'll also probably see fit to clean-up and release some other random scripts I have laying around.
The idea though is for the next 100 (week)days, I'll be dedicating 1 hour at least to coding, probably, odds are usually more but I have 5-6PM blocked on my calendar to dedicate to this specifically.

Sometimes it's easy to feel overwhelmed by your mountain of tasks and projects but with proper planning, time management, and tackling tasks one-by-one you can make real impacts that are not easy to see in the short term but are remarkable over a longer span.

The key to overcoming this is to also document along the way so you can see your progress and show what it took to get there.  This helps more easily relate what you do because as engineers/developers/fucking magicians it's sometimes difficult to demonstrate or explain our work/worth.  It also does you personal justice in detailing your methods so you can improve upon your processes and most importantly, refer back to them in case you forgot.

Sometimes it's easy to self-impose higher level tasks for simple projects, which is why I'm trying not to get too OCD with this site, but that was my Day 1 project - Get Setup.

## Day 1
### Project: Kemo Networks (this site)
### Task: Get things set up, at least on my system in Dev

- So I loaded up a new Fedora 28 VM in Virtualbox, got it all comfy with Guake and some other things.
- Then I headed on over to the Hugo documentation and installed the needed bits and Hugo.
- Found a pretty nice theme with the simplicity I had in mind
- Added architypes for my content types, which is basically just the skeleton template for your various 'hugo new' built content
- Created layouts - this shit was kinda confusing, but I think I have it figured out now.  First
  - First, check your theme because odds are they have some base layouts to use that you saw in the preview...don't rebuild the wheel
  - Next, you've got your **layouts/_defaults/{li,single,list}.html** files which are your, well, defaults.  Copy these suckers over to **layout/type_here** folder and start modifying lists and content views.
  - What's so fucking hard about simple includes and shortcodes?  Why does every "framework" have to make things difficult...
- Started adding some content to fill out the views and get the feel for things.  This is done with the hugo generator which for this site currently generates content as such:
  - hugo new posts/my-new-blog-post-title.md
  - hugo new 100-days-of-code/catchy-title-here.md
  - hugo new links/link-title.md
  - hugo new gallery/image-name.md
- This basically just copies over the architype skeleton into a new named file under that content directory.  I like the simplicity.
- What I don't like though is the rigidity...but then again I'm not supposed to get too OCD over being not able to include things at the end of a nested ul in the parent li...
- I didn't quite finish this all the way, I still need to set up a few minor things, but I'll do that tomorrow as I've already been at this for a couple more hours than what I scheduled...

