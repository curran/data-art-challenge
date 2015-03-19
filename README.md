# data-art-challenge

This document is a submission for the [Sense Your City Data Art Challenge](http://datacanvas.org/sense-your-city/), by Curran Kelleher and Emilie de Longueau of [Alpine Data Labs](http://alpinenow.com/).

The first step of our process was to fetch the data with simple API use. This is what we saw when querying for temperature data in Geneva with a resolution of 5 minutes over the past 24 hours.

|[![](images/Block1.png)](http://bl.ocks.org/curran/5f255332a9dcb9906f84) |
|:---------------:|
|[The raw data, "visualized" as text.](http://bl.ocks.org/curran/5f255332a9dcb9906f84)|

Using the data returned from the API in conjunction with a D3 Line Chart module developed as part of the [ModelJS project](), we created the following simple visualization. Clicking the link will show you up-to-date data, and will automatically update every 5 minutes. if you [run the visualization full screen](http://bl.ocks.org/curran/raw/015402cce2caa074551e/), it will automatically resize to fill the window.

|[![](images/Block2.png)](http://bl.ocks.org/curran/015402cce2caa074551e) |
|:---------------:|
|[24 hours of temperature in Geneva.](http://bl.ocks.org/curran/015402cce2caa074551e)|

Since the API only supports accessing data for a single city at a time, we used [async.js](https://github.com/caolan/async) to manage asynchronous control flow for fetching data for multiple cities (using separate API calls) then merging the result. With this approach we were able to visualize temperature for many cities in the following bar chart.

|[![](images/Block3.png)](http://bl.ocks.org/curran/015d34d6d3d562877e51) |
|:---------------:|
|[Current temperature in all available cities.](http://bl.ocks.org/curran/015d34d6d3d562877e51)|

Combining the first two visualizations and color coding marks by city yields the following visualization dashboard with a bar chart and line chart.

|[![](images/Block4.png)](http://bl.ocks.org/curran/3b811f05a0ce39d0d7cd) |
|:---------------:|
|[24 hours of temperature for all available cities.](http://bl.ocks.org/curran/3b811f05a0ce39d0d7cd)|


We wanted to try analyzing this data using [Alpine](http://alpinenow.com/). To do this, the data was first extracted into CSV format, then imported into a Hadoop file system.

|[![](images/Block5.png)](http://bl.ocks.org/curran/c65ce9880826e466d2b0) |
|:---------------:|
|[A CSV data dump.](http://bl.ocks.org/curran/c65ce9880826e466d2b0)|

The following analysis and visualizations were created using by Emilie de Longueau using Alpine. 

<img src="images/AlpineAnalysis.png">

<img src="images/BoxPlotMonth.png">

<img src="images/splom.png">
