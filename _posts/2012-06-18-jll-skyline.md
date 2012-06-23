---
layout: post
title: A Mobile Poster
video: 555
author: Zach Phillips
---

Jones Lang LaSalle's Atlanta branch needed a mobile way to browse their commercial real estate portfolio. 

What they had was a huge poster-sized InDesign document. Our job was to figure out how to get that whole poster (with more than fifty buildings and availability and agent contact information for each) into a mobile-optimized view, easy to quickly browse.

My first choice would have been to use Raphael.js to draw the buildings with Scalable Vector Graphics or Paper.js to accomplish it in an HTML5 canvas, but that kind of fanciness wasn't in the budget.

The answer was [SwipeView by Matteo Spinelli at cubiq.org](http://cubiq.org/swipeview). Spinelli is a bad-ass master of mobile javascript, and SwipeView was exactly what I needed. It's basically a seamlessly loopable carousel for the mobile web, optimized for touch and hardware-acceleration, making the swipe action silky smooth in Mobile Safari. Every bit as smooth as a native app. It also only loads the next and previous item to the currently viewed item, so it's great on memory and bandwidth as well.

I think the solution worked out really well, and it's already built into the skeleton of a Rails app, so if another client has a larger-scale use for this kind of browsing, we'll be ready to build the rest of that out. I think it's a really great way to look through products, browse directories, etc. on mobile.

I'd built in a custom search field using [jQuery.chosen](https://github.com/harvesthq/chosen/), but the native iPhone drop-down ended up performing a lot better and didn't have all of the independently scrolling div problems you have with mobile ([which Spinelli has also addressed](http://cubiq.org/iscroll-4), though his solution was too hacky an alternative for my needs).