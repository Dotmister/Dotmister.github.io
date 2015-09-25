---
layout: post
title:  "News Globe"
date:   2015-06-18 08:43:59
author: Adam Casey
categories: personal
---

News globe was a project I worked on at the Bloomberg Summer Internship Hackathon 2015 in a team of five. In 24 hours we put together a solution which scraped various news websites, linking it to geographical locations, and visualised it on a 3D globe.

![News Globe Logo](/assets/blog/newsglobe1.png)

The key aim of the project was to make understanding the geography of today's current affairs instant. We think that goal was achieved - the image below shows data collected on 31st July - 1st August.

![News Globe Demo - France Highlighted](/assets/blog/newsglobe2.png)

One of the top stories in global news at the time was the discovery of a fragment of MH-370, washed on up the beach of a French Overseas Department. The part was also being flown back to mainland France.

I worked on the frontend for this project. It was essentially [WebGL Globe](https://www.chromeexperiments.com/globe), a Google Chrome experiment. The extra work first required was to link it up to the back-end: this was relatively straight forward AJAX and then JSON parsing. Then some effort was needed to display this data on the 3D globe.

WebGL Globe by default only lets you draw a single "line" at specified lat, lng co-ordinates which has a single property of height. To represent a land-mass rather than a single point, I simply generated a fixed list of points to be drawn for each country on the map. Ideally I would have adapted WebGL Globe to draw shapes rather than simply columns, however this was not feasible in the time allotted. The generation process was slow, but once complete it could be cached and re-used.

[Check it out on GitHub](https://github.com/adamncasey/newsglobe)