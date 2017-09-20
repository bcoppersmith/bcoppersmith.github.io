---
layout: post
title: "Extremely Late City Council Election Analysis"
date: 2017-09-19 16:35:19 -0700
about: Mapping the turnout and results for District 13's City Council election on Marth 7, 2017.
---

It's time for some election analysis! And yes, I'm talkin' 'bout the big one: the race for LA Council District 13 from the Los Angeles County March 7th Consolidated Municipal and Special Election! 

Why now? Well jeez, I didn't know there was deadline.

Why this election? Only four months after the big November General Election, we elected new City Council members, who are about as local as you can go while still retaining real political power. It's also an interesting election: rising rents are causing real problems and leading to real tensions, plus, would anyone care that the [reservoir was still empty](http://www.latimes.com/local/california/la-me-silver-lake-reservoir-20150615-story.html)?

This was also the first of 7 elections for Los Angeles County voters in 2017. Oh boy.

So: how was turnout? It was fine:

<iframe width="100%" height="520" frameborder="0" src="https://ben-coppersmith.carto.com/viz/a03ec8e5-2e66-450f-9d64-918ebb0343e8/embed_map" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

The reservoir seems to act as a turnout sink -- more votes the closer you get. My guess there is that income/wealth also increases as you get closer to the water. Another factor might be polling place location; I know my polling place is at the base of the reservoir, and there's a chance that had a positive affect as well.

Of course, "good" turnout for this one is all relative. No precinct turned out more than 50% of its registered voters for this "hangover" election. Overall, 25% (32,019) of registered voters cast ballots in this election for CD13. About 67% (76,717) cast a ballot in the [November general](https://www.lavote.net/home/voting-elections/current-elections/election-results/past-election-results#06072016).

Here are the election results:

<iframe width="100%" height="520" frameborder="0" src="https://ben-coppersmith.carto.com/viz/519ce0d8-8906-4903-ad41-a34147940951/embed_map" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

Mitch O'Farrell easily won re-election, with around 60% of the vote and ~17k votes. There's no clear geographic trend to his vote, but it's clear he cleaned up in Silver Lake Village (yes, that _is_ the official subneighborhood name for south of the reservior!) and Lesser Los Feliz (I made that one up). It's also clear that there's no clear backlash to how O'Farrell is handling the reservoir; my sense was the strategy in March was to refill it ASAP and then debate if it should be further developed later. I know there was a push to make it a bigger, better park, but that doesn't seem to translate into votes. Lots of votes come from the houses around the Reservoir, and Mitch did just fine with those.

Besides O'Farrell, there were five challengers: 

* Sylvie Shain: 2nd place - ["tenant activist"](http://www.latimes.com/local/lanow/la-me-ln-council-district-thirteen-20170227-story.html)
* Jessica Salans: 3rd - It might be true that Bernie Would Have Won, but Salans, a Sanders campaign volunteer, definitely did not
* Doug Haines: 4th - [the guy behind the lawsuit that stopped construction on the Target in East Hollywood](http://www.latimes.com/local/lanow/la-me-ln-hollywood-activist-city-council-election-20161111-story.html)
* David De La Torre: 5th - a stevedore!
* Bill Zide: 6th - ["former neighborhood council president"](http://www.latimes.com/local/lanow/la-me-ln-council-district-thirteen-20170227-story.html)

O'Farrell swept nearly every precinct, winning a plurarity in all but one major precinct. De La Torre got that one -- he took the area around Frogtown with 222 votes to O'Farrell's 181. Maybe that's where the other stevedores live.

Anyway: that's all for this election. Until next time, when I go deep on the April 10, 2018 Long Beach USD and Community College District Governing Board Member Elections in early 2020.

Notes on the data:
- This was pretty basic: the Los Angeles County Registrar's website has results for all previous elections. They have a geoportal, but were missing the March 7th shapefiles when I checked, so I emailed the office to get them (and I got same day response!).
- I put the election results and precinct shapefiles into two Postgres tables and then joined on precinct_id. I plopped the resulting CSV export onto CartoDB and got a pair of easy-but-good-looking maps.
- I had to `ST_Transform` the geometries to WGS 84, but that was only thing that could plausibly pass for fanciness with the data processing.
