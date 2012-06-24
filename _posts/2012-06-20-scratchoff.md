---
layout: post
title: A Scratchoff for the Mobile Web
categories: projects
video: 44545692
author: Zach Phillips
synopsis: Our first commercial product. It lets you run custom scratchoff campaigns with prizes and odds without your customers having to download an app.
---

While working on [the mobile sweepstakes promotion for the Atlanta Hawks and British Petroleum](/work/bp-hawks), it became evident pretty quickly that this could be a good fit for a lot of companies, so we built a subdomain-based Rails app.

The first thing we had to do was find a way to leverage touch and the HTML5 canvas for creating the scratchoff (or more accurately, wipe-away or eraser) capability. It would need to function well on both iOS and Android, the two leaders in the handset market. The rest of the players are pretty hit or miss in terms of web standards support, but luckily, their marketshare is also pretty pitiful, and so we felt safe to ignore them. It's worth noting that there's a ton of fragmentation within Android itself, and so we couldn't guarantee blanket support across the hundreds of devices in that category, but our testing showed support on every device we tried, some of them as old as three years, and the vast majority running 2.3.

Our savior was a frenchman (or Belgian?) who goes by the handle of [@boblemarin](http://twitter.com/boblemarin). He had created a jQuery plugin called [jQuery.eraser](http://minimal.be/lab/jQuery.eraser/), which takes any image pass in and turns it into an HTML5 canvas element erasable by both cursor and (most importantly for us) touch.

We only had to make a few tweaks to the code, allowing it to use images optimized for Retina displays, and the result was really fun. I found myself playing it over and over simply because it was fun to scratch off the image. It really feels like a native app running in the iPhone's browser.

The rest of the process entailed figuring out how to return a _weighted_ random result (weighted by the odds of winning each prize) and using cookies and some server-side code to prevent abuse.

[mobilezen](http://mobilezen.com) (my first client after going independent three years ago) offered to go into a partnership where they would handle the sales, billing, and support, so the Kitchen could focus only on making the game as awesome as it could be.

It's been sold several times since then, but we're still looking for a big client who wants to take their mobile game to the next level. You see sweepstakes games on virtually every soda bottle and fast food cup in the world, but they're usually terrible experiences where you have to go to some website and type in a 419 digit alphanumeric code to find out whether you've won a _chance_ to win a backpack or something like that. The immediacy and touchability of [Scratchoff.me](http://scratchoff.me) is a greatly superior experience and really gives customers something fun to do and a tremendously positive brand impression.