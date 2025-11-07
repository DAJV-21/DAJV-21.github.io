---
name: Homework 5 Project
tools: [Python, Altair, vega-lite]
image: assets/pngs/cars.png
description: This shows two interactive plots about professional licenses data iin the US.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Example including vega-lite

The plots show data about issued licencses in the US. Both of these plots were built using a subset of the dataframe with only two columns, to reduce the size of the data for the plot. 

The first plot shows the number of issued licenses per year from 1912 to 2022, in a line plot format. The information of this graph was obtained by changing the variable of the 'Original Issue Date' to date and extracted only year in a variable called 'Original Issue Year', which became part of the subset used.In the encodings, we adjusted the Axis, to make the plot undestandable. As this first plot is a line plot of temporal, variable 'Original Issue Year' was assigned to the x-Axis as ordinal data, to keep order. Moreover, for this axis, we only showed one label every 5 years at an angle of 0, to avoid clutter and keep them straight.Meanwhile, the y-axis showed the count of issued licenses as cuantitaive data. Lastly, we added a tooltip so the user can see the details of each datapoint. Everything was built with the default colormap because this graph does not need to emphasize on one year. .However, this plot intearcts with the second one.

<vegachart schema-url="{{ site.baseurl }}/assets/json/Home5.json" style="width: 100%"></vegachart>


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>
