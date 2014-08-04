---
layout: post
title: Wikis and coding and ldap, oh my! <_<
category : [Code, health]
tagline: 
tags : [cid, eggdrop, extsock, ldap, php, Projects, wiki]
timestamp: 1237139040
---
Yeah so that sums it up nicely. I devoted an entire week to coding and ice cream. How sweet is my life? Actually don't answer that please...

So it seems Anope has a lot of things that are remnants of a previous life. Lots of old data in Zbot, lots of old stuff on the wiki...I spent an entire evening combing through a database looking for entries that were still useful for an infobot - maybe 200 still applied out of over 1000. The wiki needs a lot of work too since most of it still applies to 1.6/1.7. With any luck that will be in better shape by next weekend. Depends on how this mono things goes I suppose.

I applied some more changes to iFail...what was once a dedicated bmotion eggdrop has now become useful. It reminds me of the good old days when people actually made eggdrops do things other than be annoying.

There's also some shiny new ldap auth stuff for the forums/wiki/bug tracker/etc that should be fun. After some minor clusterfuckery, things seem to be going rather well.

I've also started cleaning up the extsock stuff again out of boredom. For those of you who don't know what that is, it's basically a module that connects to Anope and makes a socket which allows you to interact with services from a website. That's one of few things I'll give Atheme credit for - they do the whole XMLRPC thing which is hella more useful than SQL. Live SQL is nice and all, but it doesn't really allow you to interact with services...you can just mess with the databases. By using a socket to talk directly to services, you get to do cool stuff like send globals without even being on the server. Win. ^_^

There's also a spiffy CID modules that keeps track of sessions. I was working on the PHP for that a while back but I seem to have lost bits of it >_> I suppose that'll teach me to have like 23498752349872345 computers and even more external hard drives/thumb drives. I should sort my e-life out. But it's pretty neat...just needs a little bit of work to get it working how I'd like. the biggest things are sessions and the search feature. It'd also be nice if it didn't display anything when the timeOff was 0. That makes it look like they signed off in 1969...most of us weren't even born then and IRC wasn't even a concept.

Thanks to Rob for the C/Anope (and some PHP!) side of things =]