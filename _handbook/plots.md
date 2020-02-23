---
title: "Plots and Variables"
permalink: /handbook/Plots-and-Variables/
header:
    teaser: /images/teaser/plot.png
---
This page almost exclusively uses citations from the book *Data Analysis with Open Source Tools* by *Philipp K. Janert*

## Single Variables (Univariate)

> *With univariate data, we usualy only care about the overall shape of the distribution:*
> - Where are the data points located, and how far do they spread? What are typical, as well as minimal and maximal, values? 
> - How are the points distributed? Are they spread out evenly or do they cluster in certain areas? 
> - How many points are there? Is this a large data set or a relatively small one? 
> - Is the distribution symmetric or asymmetric? In other words, is the tail of the distribution much larger on one side than on the other? 
> - Are the tails of the distribution relatively heavy (i.e., do many data points lie far away from the central group of points), or are most of the points—with the possible exception of individual outliers—conﬁned to a restricted region? 
> - If there are clusters, how many are there? Is there only one, or are there several? Approximately where are the clusters located, and how large are they—both in terms of spread and in terms of the number of data points belonging to each cluster? 
> - Are the clusters possibly superimposed on some form of unstructured background, or does the entire data set consist only of the clustered data points? 
> - Does the data set contain any signiﬁcant outliers—that is, data points that seem to be different from all the others? 
> - And lastly, are there any other unusual or signiﬁcant features in the data set—gaps, sharp cutoffs, unusual values, anything at all that we can observe?

How do we analyze this data?

### Dot/Jitter Plot - Key Points
- Whenever a certain value occurs more than once in the data set, the corresponding data points fall right on top of each other, which makes it impossible to distinguish them. This is a frequent problem, especially if the data assumes only integer values. The problem is avoided by shifting each point by a small random amount from its original position resulting in a **Jitter Plot**
-

