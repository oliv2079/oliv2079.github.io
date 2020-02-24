---
title: "Plots and Variables"
permalink: /handbook/plots-and-variables/
header:
    teaser: /images/teaser/plot.png
---


Pros and Cons of using different types of plots depending on the data.

## Single Variables (Univariate)

With univariate data, we usualy only care about the overall shape of the distribution

> [Questions to ask when considering single variables](/handbook/plots-and-variables/univariate-questions/)


### Dot Plot

Whenever a certain value occurs more than once in the data set, the corresponding data points fall right on top of each other, which makes it impossible to distinguish them. This is a frequent problem, especially if the data assumes only integer values. The problem is avoided by shifting each point by a small random amount from its original position resulting in a *Jitter Plot*

Makes it hard to read off quantitative information from the graph. In particular, if we are dealing with larger data sets, then we need a better type of graph, such as a *Histogram*.

### Jitter Plot

- It is important that the amount of “jitter” be small compared to the distance between points so as not to shift them signiﬁcantly from their true location.
- We can jitter points in either the horizontal or the vertical direction (or both), depending on the data set and the purpose of the graph
- Open rings are most easily recognized as separate even when partially occluded by each other. Filled symbols tend to hide any substructure when they overlap, and symbols made from straight lines (e.g., boxes and crosses) can be confusing because of the large number of parallel lines
- With larger data sets, we need a better type of graph, such as a *Histogram*.

### Histogram

- *Bin Width:* There is no simple rule of thumb that can predict a good bin width for a given data set; typically you have to try out several different values for the bin width until you get a good result. Assuming a Gaussian Distribution, one can start with [Scott’s rule](https://en.wikipedia.org/wiki/Histogram#Scott's_normal_reference_rule){:target="_blank"} for the bin width $$w=3.5*\sigma / \sqrt[3]{n}$$ where $$\sigma$$ is the standard deviation of the distribution and $$n$$ is the number of points.

- In an *unnormalized histogram*, the value plotted for each bin is the absolute count of events in that bin
- In a *normalized histogram*, we divide each count by the total number of points in the data set, so that the value for each bin becomes the fraction of points in that bin
- *Differing Bin Widths:* narrower where points are tightly clustered but wider in areas where there are only few points. Appealing when the data set has outliers or areas with widely differing point density. *Problem*: should you display the absolute number of points per bin regardless of the width of each bin; or should you display the density of points per bin by normalizing the point count per bin by the bin width?

- To compare two or more data sets, draw [*frequency polygons*](#frequency-polygons): remove the boxes, and draw symbols where the top of the boxes would have been. (The horizontal position of the symbol should be at the center of the bin.) Then connect consecutive symbols with straight lines. Frequency polygons are almost always a better choice than a histogram from boxes. If you nevertheless choose to use boxes, it is best to avoid ﬁlling them.
- When comparing several data sets in the same graph, always use a frequency polygon, and stay away from stacked or clustered bar graphs, since these are hard to read.

### Frequency Polygons
[Example Plot](/images/handbook/frequency-polygons.jpg "Source: math.libretexts.org"){: .btn}{: .text-right}
- When comparing several data sets in the same graph, always use a frequency polygon, and stay away from stacked or clustered bar graphs, since these are hard to read.


## Sources

[*Data Analysis with Open Source Tools*](http://shop.oreilly.com/product/9780596802363.do){:target="_blank"} by [*Philipp K. Janert*](https://www.oreilly.com/pub/au/933){:target="_blank"}

