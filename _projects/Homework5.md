---
name: Homework 5 Project
tools: [Python, Altair, vega-lite]
image: assets/pngs/Licenses.png
description: This shows two interactive plots about professional licenses data in the US.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Licenses situation across the years

The plots show data about issued licenses in the US. Both of these plots were built using a subset of the dataframe with only two variables(columns) created in the data manipulation, to reduce the size of the data for the plot. 

The first plot shows the number of issued licenses per year from 1912 to 2022, in a line plot format. The information of this graph was obtained by changing the variable of the 'Original Issue Date' to date and extracted only year in a variable called 'Original Issue Year', which became part of the subset used. In the encodings, we adjusted the Axes and showed a detail of each datapoint, to make the plot understandable. As this first plot is a line plot of temporal, variable `Original Issue Year` was assigned to the x-Axis as ordinal data, to keep order. Moreover, for this axis, we only showed one label every 5 years at an angle of 0, to avoid clutter and keep them straight. Meanwhile, the y-axis showed the count of issued licenses as quantitative data. Lastly, we added a tooltip so the user can see the year of each datapoint. Everything was built with the default colormap, which is blue, because this graph does not need to emphasize on one year. The variable used for this column was the `Original Issue Year`, which showed this characteristic for every license. To obtain this, we changed the `Original Issue Date` variable to a datetime type  column and dropped the missing values, from which we extracted only the year for the new column. However, through its brush, this plot interacts with the second one.

The second plot is a horizontal barplot, shown below the line plot. Each bar shows a category of license, and its respective length is a representation of the count of licenses that belong to that category.The `Status_Group` variable  is encoded on the y-axis as a nominal category displaying each license status its corresponding bar, while the x-axis encodes the quantitative count of licenses for each status. The tooltip encoding displays the count of licenses when hovering over a bar, to avoid any confusions due to the X-axis scale. The color variable used is `Status_Group`,  allowing users to assign a color to each of its categories to help users distinguish between the different license status types. The colormap was not defined because, based on the type of data, Altair is able to choose one by default, which was adequate for our graph. If a brush is not selected, the barplot represents the cases of all the years in the dataset. However, the user selects a range of years with the brush, the barplot automatically filters to show the status distribution only for that selected period.

One transformation was made for this plot. The column `Status Group` was created only for this plot and derived from the variable `License Status`, which was part of the original dataset. This transformation permitted the reduction of the number of labels, which would make it difficult to analyze each of them. For example, several termination-related labels such as "CANCELLED", "CLOSED", "CHANGE OF OWNERSHIP", "TERMINATED VALID REASON", and others were all grouped under "Terminated". This transformation simplified interpretation, and made the bar chart more readable. 

Finally, the plot's connection has a purpose that is intended to be useful for the user. The brush interactivity between the two graphs makes the graph more interesting because it lets the user personalize the data according to their needs. The interactivity allows the user to have a detailed understanding of the licenses status behavior within a period of time. This allows the user to look for patterns as sudden shifts in active licenses, easily, to test hypotheses such as “Does inactivity spike in certain periods?” . In short,the interactivity helps give more context to the license situation across different periods.


<vegachart schema-url="{{ site.baseurl }}/assets/json/Home5.json" style="width: 100%"></vegachart>


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/DAJV-21/DAJV-21.github.io/blob/main/python_notebooks/Homework5.ipynb" text="The Analysis" %}
</div>
