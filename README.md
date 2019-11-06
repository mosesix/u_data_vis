# README.md for Udacity Data Visualisation Project

## SUMMARY
The data visualisation shows the relationship between per capita CO2 emissions per country compared to that country's Human Development Index (HDI) and how this relationship changes over time. The data used is from another Udacity project (Investigate a Dataset) and was selected because it showed some interesting features: a strong but non-linear relationship between the variables and an interesting change over time which is difficult to visulaise using static visualisations (such as MatPlotLib). The key message for users to take away is that more developed (high HDI) countries have historically emitted more CO2, but that these emissions are decreasing over time with an increase in HDI. The visualisation also has exploratory features (the mouseover for each bubble) so that users can identify other interesting features.

## DESIGN
### Version 1
A bubble chart was selected with CO2 emissions on the x-axis and HDI on the y-axis in order to show the correlation between these two pieces of data. CO2 emissions were also double-encoded in the size of the bubble as this is the most important information in the visualisation. Each bubble is coloured according to the geographic region to allow the user to identify their own patterns in the data: for example, the close grouping of European Union countries and the high emissions of some middle eastern countries. The user can also access additional information about each bubble with a mouseover. An animation of how the correlation changes over time is the most important feature of the visualisation as this is something which is very difficult to see in standard, static charts. The animation is automatic (and continuous in a loop) with progress shown in bars on the left of the main chart by changing the bar colour. Clicking on the bars jumps to the indicated year and pauses (or resumes) the animation. The bars also contain information about the average CO2 emissions for each year in the length of the bar showing how the average (per country) emissions have risen and then started to fall over time.
### Version 2
Following the feedback (see below) the bubble chart was modified to include the following features:
* Explanatory text explaining what the chart shows (below the title), how to interact with it (below the legend) and what conclusions were drawn (at the end).
* Bubble size decreased to make it easier to see individual countries.
* Persistent bubbles with low opacity added for 1990 data - "ghost" bubbles for reference during the the animation
* Legend moved below the chart.
* Opacity of the bars on the side chart decreased so that the years could be more easily seen.
* X-axis with label and tick marks added to the side chart to make it easier to understand what the length of the bars means

## FEEDBACK
Feedback was collected from colleagues and friends working in multiple different fields via a [Google Form](
https://docs.google.com/forms/d/1_g-Ikr2lqmJjPfR7hKHCshNXgxNZ_h-cHlfcKX0IJwY/)
The key pieces of feedback are noted below:
* Clearer explanation of what the chart is showing and how to navigate.
* Ability to compare to previous years.
* Make it easier to see (and hover over) individual bubbles.
* Ability to filter the bubbles (by region).

## RESOURCES
The dataset used for the visualisation is from http://Gapminder.org. It was wrangled in Python using Pandas as part of the Udacity Investigate a Dataset project. Additional code was added to further treat the data for this project, including melting the pandas dataframes from wide to long format, and to export as two CSV files. These were combined and modified in Excel, including adding a lookup for the regions corresponding to each country based on UK HMRC data available here https://www.uktradeinfo.com/CodesAndGuides/Documents/Country_region.xls.

The Dimple.js documentation [dimplejs.org] was consulted extensively with whole sections of code from the documentation used in the index.html file, especially for the storyboard control [http://dimplejs.org/advanced_examples_viewer.html?id=advanced_storyboard_control]. Any reused code is indicated in the index.html file.

