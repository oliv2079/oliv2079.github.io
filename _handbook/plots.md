---
title: "Plots and Variables"
permalink: /handbook/plots-and-variables/
header:
    teaser: /images/teaser/plot.png
---


Pros and Cons of using different types of plots depending on the data.

## Summary Statistics
- Mean, Median, Standard Deviation, Percentiles, ...
- Apply only under certain assumptions and are misleading
- Because something is convenient and popular is no reason to follow suit.
- Apply only to distributions that have a single, central peak (unimodal distributions). If not fulﬁlled, then conclusions based on simple summary statistics will be wrong
- Prefer Standard Deviation over Variance: Both measure for the location, and the measure spread will have the same units, which are also the units of the actual data
- Expect 2/3 of data is within 1 sd and 99% within 3 sd (unless not symmetric or many outliers)

- Median, Quantiles, Percentiles: More Flexible and Robust
- Use these (over mean, sd, ...) whenever distribution is not symmetric or has important outliers.

- Inter Quantile Range (IQR - distance between the 75th percentile and 25th percentile) is most frequently used.



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

- Common 
- intuitive interpretation
- Easy to generate
- Not unique (e.g. varies depending on Bin Width)
- Ragged and not smooth (Cannot be evaluated as a function)
- Do not handle outliers well

- *Bin Width:* There is no simple rule of thumb that can predict a good bin width for a given data set; typically you have to try out several different values for the bin width until you get a good result. Assuming a Gaussian Distribution, one can start with [Scott’s rule](https://en.wikipedia.org/wiki/Histogram#Scott's_normal_reference_rule){:target="_blank"} for the bin width $$w=3.5*\sigma / \sqrt[3]{n}$$ where $$\sigma$$ is the standard deviation of the distribution and $$n$$ is the number of points.


*Differing Bin Widths:* narrower where points are tightly clustered but wider in areas where there are only few points. Appealing when the data set has outliers or areas with widely differing point density. *Problem*: should you display the absolute number of points per bin regardless of the width of each bin; or should you display the density of points per bin by normalizing the point count per bin by the bin width?

*unnormalized histogram*: the value plotted for each bin is the absolute count of events in that bin

*normalized histogram*: we divide each count by the total number of points in the data set, so that the value for each bin becomes the fraction of points in that bin

*two or more data sets*: draw [*frequency polygons*](#frequency-polygons): remove the boxes, and draw symbols where the top of the boxes would have been. (The horizontal position of the symbol should be at the center of the bin.) Then connect consecutive symbols with straight lines. Frequency polygons are almost always a better choice than a histogram from boxes. If you nevertheless choose to use boxes, it is best to avoid ﬁlling them.
- When comparing several data sets in the same graph, always use a frequency polygon, and stay away from stacked or clustered bar graphs, since these are hard to read.

### Frequency Polygons 
- [Frequency Polygons](/images/handbook/frequency-polygons.jpg "Source: math.libretexts.org")
- When comparing several data sets in the same graph, always use a frequency polygon, and stay away from stacked or clustered bar graphs, since these are hard to read.

### Kernal Density Estimates (KDE)
- *Area* under curve formed by a kernel must be 1 -> properly normalized.
- We are free to use the kernel that is most convenient
- Must move the kernel to the position of each point by shifting it
- Must choose the kernel bandwidth, controlling the spread of the kernel function. 
- Large data sets can lead to performance issues
    -If this becomes a problem, use simpler kernel function or don't evaluate a kernel if the distance $$x−x_i$$ is signiﬁcantly greater than the bandwidth h.
- Is unique
- Is also smooth (depending on kernel)

### Cumulative Distribution Function (CDF)
- [CDF](/images/handbook/cdf.png "Data Analysis with Open Source Tools - Page 27")
- A Histogram (or KDE) can be misleading (The eye is much better at judging distances than areas)
- Less wiggly than a histogram (or KDE), but contains the same information (and less noisy). 
- No binning, they do not lose information meaning more faithful representation
- A CDF is unique for a given data set. 
- Comparing bell-shaped curves in a histogram is hard. Comparing corresponding CDFs is much more conclusive.

### Probability Function & QQ Plot
- [Example](/images/handbook/probabilityplot.png "Data Analysis with Open Source Tools - Page 24")
- Purpose: Determine whether a given data set stems from a speciﬁc, known distribution
- Advanced, specialized technique
- You should evaluate whether you really need them

### Rank Order Plots & Lift Charts
- [Rank Order](/images/handbook/rankorder.png "Data Analysis with Open Source Tools - Page 24"), [Pareto](/images/handbook/pareto.png "Data Analysis with Open Source Tools - Page 24")
- When the independent variable does not have an intrinsic ordering, it is often a good idea to sort entries by the dependent variable
- Sorting by the dependent variable is useful when independent variable has no meaningful ordering relation
- Cumulative distribution curve is occasionally referred to as a lift curve (It shows the “lift” from each entry or range of entries)


## Sources

[*Data Analysis with Open Source Tools*](http://shop.oreilly.com/product/9780596802363.do){:target="_blank"} by [*Philipp K. Janert*](https://www.oreilly.com/pub/au/933){:target="_blank"}

