---
layout: post
title:      "PhishBook(working title)...the App."
date:       2019-06-20 13:42:22 +0000
permalink:  phishbook_working_title_the_app
---


This was a particularly fun project to build.  It allowed me to combine my new love of coding with my old (yet still enduring) love of the band Phish.  In short the app is a place where fans can create profiles and reminisce about old times, or more recent times at Phish shows.  They can do this by leaving "memories" (posts) about experiences they had at a particular show, or during a particular run. There are lots of fans who, like me, have spent a large portion of their life following this band around, making friends and creating some awesome experiences along the way.

The biggest obstacle for me was understanding and finding the appropriate associations to use between my models. 
1)I had a years model, which had many shows.  
2)A Show model, which belonged to years and had many fans. 
3)A Fan(user) model which had many shows and many memories
4)A memories model which belonged to a show and a fan.

The toughest association was the shows to fans, and fans to shows.  Originally I had Fan has_many  :shows and Show has_many :fans.  But that wasn't working out for me.  The problem was anytime I had added a show to fans collection, it was being removed from another fan. I.e. A show could only belong to one fan.  Of course this caused some panic for me, because I was sure I was right in my associations.  After my panic subsided, I did some research and discovered the "has_and_belongs_to_many" association and that corrected my issue.  PHEW!!!  from there on out it was pretty smooth sailing.  

Another thing I learned to do during this project is to just use and play with the app at times to a) make sure you're on track and its working as it should. b) to see if theres any features or functionality that should be added to improve your app.  Unlike my CLI project, I did a fair amount of planning before I wrote any code.  This was definitely beneficial but even the best thought out plans can overlook somethings.  I think this is all part of developing your "style" or "process".  Planning is good but don't be afraid to change the plan or divert from the plan if it makes sense.  Even at the times when I wanted to "be done" with a certain portion, It was useful to spend a little extra time making sure things were right before moving on.  

This was another fun project and I'm pretty excited to developing this app and make future improvements.

Cheers
