---
layout: event
category: event
title: Collaborative Cartography Night-FixWikiMaps
rsvp: http://www.meetup.com/MaptimeNYC/events/225740734/
---

![Collaborative SQL](/img/2015-10-07/20151007_205519.jpg)  

Anyone who has explored Wikipedia in-depth has come across the sometimes wonderful, sometimes horrid map and image attachments to articles. As it turns out, there's a small group of people interested in making a design dent in this aspect of Wikipedia, like [FixWikiMaps](http://fixwikimaps.tumblr.com) and they have set up sites and workflows for improving Wikipedia maps, one at ta time. 

So Maptime NYC brought everyone together and chose two of them to tackle, sourced form FixWikiMaps. The first, a map of the ten most populous cities in the US, was a map that had been used for multiple purposes, with some unnecessary regional coloring and needed a facelift. The second, a map of the Parishes of Louisiana, was hard to read and was missong some potentially good information, like Parish seats. 

We did a quick intro and then critiqued the maps individually, making some starting decisions on design and data. Brandyn had collected a few necessary pieces beforehand, making it easier to speed through. 

We broke into two groups, one for each map. 

[each breakout leader writes this?]

####Louisiana Parishes Map  

In the Parishes group, the data available was the parish polygons, the cities, towns and villages point file and state polygons. We discussed the data we had and the goals and decided on CartoDB as the tool. We briefly discussed Mapublisher, but decided it was too restrictive in access. We assembled what we had. The state files were too coarse and looked clunky. Someone went to find better data for just the surrounding states. We also realized a lot of water features weren't in the map (like the form-defining Lak Ponchatrain) and went seeking complete data files for those. We ended up with some great Delta wetlands polygons that showed LA as it actually is. Next, the cities. We had pulled too many intentionally from OSM using Overpass API. We ended up deciding to only pull the parish seats and major cities (for orientation). We narrowed the selection with SQL and then our time was up! To be continued.  

*Results*:  
![](/img/2015-10-07/parishes_afterMaptime.png)  
**#breakWikiMaps**.

####Top Ten Populous Cities in the USA Map  

...text summary and code snippets...  

*Results*:  
![](/img/2015-10-07/top-ten-us-populous-cities.png)

We then got together and had a brief discussion of the adventure, determining it was a great way to get to know mapping together. 



