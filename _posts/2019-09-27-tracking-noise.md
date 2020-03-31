---
layout: post
title: Tracking NYC's Biggest Nightlife Noisemakers
subtitle: by Zhenya Warshavsky   
image: /img/nyc_skyline.jpg
gh-repo: https://github.com/zwarshavsky/311NoiseComplaints
# gh-badge: [star, fork, follow]
# tags: [test]
comments: true

---

# Tracking The Fun Noise in NYC  


As co-founder of sound system design and acoustics consulting startup __[Stampede Sound](http://www.stampedesound.com)__ here in NYC, one of the principal goals of our operation has been to reduce noise transmission for small clubs and bars in the city while improving sound quality with our proprietary speakers and acoustical knowledge. Of all places to achieve this in the US, NYC is likely the most challenging: high population density, hundreds of bars and venue spaces in close proximity to residential spaces, and constantly changing neighborhood boundaries. 

A low density part of town can transform into an entertainment center and population center within just a few years and with it, shifting expectations for residents of that neighborhood. Both the businesses that serve the residents and new residential property construction are in a complicated dance with each other.    

Beyond the incredible cost of operating a bar or nightclub, there is one threat to the longevity of these establishments that is most existential: 311 Noise Complaints. No matter how successful, a sustained period of 311 Noise Complaints from residential neighbors can permanently shut down the operation.   

To track down the biggest offenders in this business space would be a huge boon not just for my company but any services that attempt to improve a part of the urban entropy which keeps the neighbors and businesses biting their fingernails. 

Come, the __[NYC Open Data](https://opendata.cityofnewyork.us/)__ 
 initiative's __[311 Noise Complaint Dataset](https://nycopendata.socrata.com/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9)__. 

After filtering the list down to the relevant data points, we're down to the following:

<img src="/img/pre_list_snippet.png" width="40%">

We turn it into a Dataframe, run the __[Google Maps Places API](https://developers.google.com/places/web-service/intro)__ against these addresses and get the following list: 


<img src="/img/list_snippet.png" width="50%">

We then create a "Rank" column which allows us to rank the top 100 places with a "1" to "100" ordinal scale. 

![rank](/img/rank.png)


We are now ready to plot our points utilizing the __[jupyter-gmaps API ](https://jupyter-gmaps.readthedocs.io/en/latest/index.html)__. The visualization tool which reveals the establishment name, its noise rank and its location can be immediately utilized by my sales team. An invaluable tool for lead generation.  

![map_3](/img/map_3.png)


The visualization reveals nightlife noise hotspots and a multitude of other location data that can be applied to other NYC Open Data datasets for further analysis.  


## Sample Dashboard View

For each specific sales cycle, we can generate a graph providing historic noise complaint trends for each business and can be generated for __[Stampede Sound's ](http://www.stampedesound.com)__ existing clients for true on-the-ground field testing. 

![Graph](/img/graph.png)
