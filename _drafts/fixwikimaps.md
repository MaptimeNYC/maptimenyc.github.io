---
layout: event
category: event
title: Collaborative Cartography Night-FixWikiMaps
rsvp: http://www.meetup.com/MaptimeNYC/events/225740734/
---

####Takeaways  
>1.  Everyone got to contribute.  Many skills go into creating a map, which means there's room (and need!) for all kinds of contributions.
>2.  
>3.  
>4.  (something about difficulty in getting maps to SVG?)  

![Collaborative SQL](/img/2015-10-07/20151007_205519.jpg)  

Anyone who has explored Wikipedia in-depth has come across the sometimes wonderful, sometimes horrid map and image attachments to articles. As it turns out, there's a small group of people interested in making a design dent in this aspect of Wikipedia, like [FixWikiMaps](http://fixwikimaps.tumblr.com) and they have set up sites and workflows for improving Wikipedia maps, one at a time. 

So Maptime NYC brought everyone together and chose two of them to tackle, sourced form FixWikiMaps. The first, a [map of the ten most populous cities in the US](https://en.wikipedia.org/wiki/List_of_United_States_cities_by_population), was a map that had been used for multiple purposes, with some unnecessary regional coloring and needed a facelift. The second, a [map of the Parishes of Louisiana](/img/2015-10-07/Louisiana_parishes_map.jpg), was hard to read and was missing some potentially good information, like Parish seats. 

We did a quick intro and then critiqued the maps individually, making some starting decisions on design and data. Brandyn had collected a few necessary pieces beforehand, making it easier to speed through. 

We broke into two groups, one for each map. 


####Louisiana Parishes Map  

In the Parishes group, the data available was the parish polygons, the cities, towns and villages point file and state polygons. We discussed the data we had and the goals and decided on CartoDB as the tool. We briefly discussed Mapublisher, but decided it was too restrictive in access. We assembled what we had. The state files were too coarse and looked clunky. Someone went to find better data for just the surrounding states. We also realized a lot of water features weren't in the map (like the form-defining Lak Ponchatrain) and went seeking complete data files for those. We ended up with some great Delta wetlands polygons that showed LA as it actually is. Next, the cities. We had pulled too many intentionally from OSM using Overpass API. We ended up deciding to only pull the parish seats and major cities (for orientation). We narrowed the selection with SQL and then our time was up! To be continued.  

#####Results  
![](/img/2015-10-07/parishes_afterMaptime.png)  
*#breakWikiMaps*.

####Top Ten Populous Cities in the USA Map  

For this map we decided that we wanted to change the coloring scheme, add more context to the map, and improve labels.  

#####Tools  
*CartoDB:*  We decided to use [CartoDB's Print API](http://blog.cartodb.com/static-maps/) because it let us store and style our data.  CartoDB's Print API also let's us print static maps for the public domain, which is crucial for submitting to WikiMedia (and awesome!).  

#####Data  
* Cities:  [OpenStreetMap](https://www.openstreetmap.org), accessed using [OverPass Turbo](overpass-turbo.eu).  
* States:  [Natural Earth](http://www.naturalearthdata.com/) 1:50m Cultural Vectors---Admin 0- Countries.    
* Countries:  [Natural Earth](http://www.naturalearthdata.com/) 1:50m Cultural Vectors---Admin 1- States/Provinces.    

#####Process  
Here's a couple cool tricks we were able to do using CartoDB:  

Reprojected to Albers Equal Area Conic for better representation of our states' data.  

{% gist 99a05d315b9fce7876bb%}

Custom label placement for fine-tuned display using CartoCSS.  

{%gist 4fb6f3480d73e3850073%}

#####Results  
![](/img/2015-10-07/top-ten-us-populous-cities.png)

Our two map groups came together after the hack night to share our progress and discuss challenges and successes.  Overall, we decided that working on making maps together is a blast and we've decided to keep an ongoing FixWikiMaps project going at all our maptimes for members to jump in on and hack over.  



