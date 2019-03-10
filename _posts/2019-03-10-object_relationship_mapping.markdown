---
layout: post
title:      "Object Relationship Mapping"
date:       2019-03-10 20:06:12 +0000
permalink:  object_relationship_mapping
---



An ORM is essentially a database to the objects mapped to it.  It is a way to store data between multiple objects, and relate those objects.

For example, lets look say we had a system that managed Media.  There are lots of different systems out there for this, all with various features and bells & whistles.  However, at their core, these systems must be able to store data, understand relationships, and return the data to a user.  The system does not "make" the relationships happen, the user must input the data and/or metadata and in some cases design the relationship.

Lets say we have an Artist.  We'll call this artist Phish.  Even before they write a song or even do anything they are an object.  A object made up of People(another object).  So if set up properly, each band member should be an object that belongs to the band(Artist). At this point, we could enter Phish into the system, and relate the people in the band.

Most bands need to actually do something though, so Phish have songs.  This is a pretty easy relationship to understand, all bands have songs, right?  Of course, Songs are also objects.

So if Phish have 1 Song, and that data is entered into our system, we'll get that 1 Song back if we search for Phish.  

But over the course of time, Phish writes many songs.  Those songs belong to Albums (another object), which belong to Phish.

So if I go into our system, I can search a particular Song object, which should return with the appropriate Artist and Album.  You can also search by Song, or by Album and receive the appropriate data in return.  You may also want to store information about the technical specs of the media.  Perhaps its filetype, size, length, sample rate, bit rate, where and when you acquired the song, etc...

Great, now when we search Phish, we get all the relevant data as it relates to their Songs and their Albums.

But now Phish start making music Videos (videos being another object).  In our system we want to be able to get ALL the media that relates to a particular object, not just one media type, right?  So a music video would still belong an Artist and should be related to the artist.   The argument could be made that the Video belongs to a Song.  However I would say the song in the video is another instance of the Song, because it's in two distincting different media types (video & audio).

Without ORM this data would be stored in multiple locations potentially across multiple servers in multiple locations.  A person would need to know how to relate this data themselves and need to do so repeatedly.  This also potentially leads to data being lost or duplicated and lead to inefficiencies in your system and workflow.
