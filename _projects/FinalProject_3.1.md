---
name: Visualization for the public
tools: [Python, Altair, vega-lite]
image: assets/pngs/Map_DC.png
description: This page shows data on crime incidents in Washington, D.C. during 2025.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Crime in Washington, D.C.

### Created by: Daniel Jimenez, Sankirtana Ravichandran, Jenna Chen


##### Note: For visualizing all the graphs' characteristics correctly, click the sun button located the top right part, next to the about button. 


<vegachart schema-url="{{ site.baseurl }}/assets/json/CentralViz.json" style="width: 100%"></vegachart>


Above is a visualization showing all crimes committed in Washington, D.C. in 2025. The graph divides all crimes into nine categories based on the type of offense. Some examples of these offenses include theft, arson, and assault. Based on the colors in the bar graph, you can see what time of day each of these crimes was committed at. If you are curious to learn more about the relationship between the type of crime and the time of day it was committed, you can click on the color that corresponds to the time of day you are interested in. The graph will change only to show you the crimes committed during that time of day. You can see the different times of day in the legend on the right-hand side. If you want to view all crimes, regardless of the time of day they were committed, at once, click the white space between the columns. 

<img src="{{ site.baseurl }}/assets/pngs/Over-18-new.png" width="650" height="650">

In the contextual visualization section, you will see a map of D.C. homicides for 2021. This image was created by the D.C. Policy Center shown in the next [link](https://www.dcpolicycenter.org/publications/homicide-exposure-maps/). You can use this image to better understand which regions of Washington, D.C. are most prone to criminal activity, in this case, specifically homicides. This visualization serves as a baseline for crime information that you can use in many ways. If you are planning to move to Washington, D.C., this image may help you think about which neighborhoods you want to live in or avoid. If you are interested in learning about policing patterns, this visualization may serve as a starting point and can be used alongside other datasets to help identify them. While this visualization provides powerful information about crime in D.C., it is essential to recognize that it includes only homicides from 2021 and may be limited in its ability to capture broader crime patterns.  

<vegachart schema-url="{{ site.baseurl }}/assets/json/ContextualViz.json" style="width: 100%"></vegachart>

The second contextual visualization highlights the specific neighborhood groupings (or clusters) in Washington D.C. By hovering over the map, a pop-up will list which neighborhood is located in that particular neighborhood cluster. For example, Howard University is in Cluster 3, Georgetown is in Cluster 4, George Washington University is in Cluster 5, Downtown and Chinatown are in Cluster 8, American University Park is in Cluster 11, Union Station is in Cluster 25, and Capitol Hill is in Cluster 26. The bar graph to the right of the map displays the area in square miles of each neighborhood cluster, ordered by number of cluster, so users can find the clusters quickly. You can select a specific neighborhood cluster from the dropdown menu underneath the map. Selecting a specific cluster from the dropdown will highlight that cluster on the map and on the bar graph.


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://catalog.data.gov/dataset/crime-incidents-in-2025" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/DAJV-21/DAJV-21.github.io/blob/main/python_notebooks/Workbook%20(1).ipynb" text="The Analysis" %}
</div>
