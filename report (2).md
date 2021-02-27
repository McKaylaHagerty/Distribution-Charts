Homework 5 
================
McKayla Hagerty

CS 625, Fall 2020 

***Observable Notebook:*** https://observablehq.com/@mckaylahagerty/homework-5 

## Part 1 - NYT Mask Usage Survey dataset

### Boxplot

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/1b.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/1b.png*

This chart shows the survey results for the mask usage for 3,142 counties in the United States in a boxplot. Here we can easily compare quartiles between the frequency categories and get a sense of the distribution of each. The median proportion of people always wearing masks is more than 25% higher than all other categories. The median proportion increased with each increase in mask wearing frequency. Also, the always category is most normal in its distribution and has the largest range. This idiom is a good fit for quick comparisons between frequency categories. Likert Scale survey questions, especially with 5-point scales, tend to not allow for enough distinction between categories to portray a true value. Therefore, a comparison between the categories may not lead to accurate conclusions. 

### Histograms

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/1h.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/1h.png*

Histograms are like bar charts except the values on the x-axis are numerical and split into bins. These histograms separate the proportions into bins of 0.02 and 0.05, respectfully. These charts show the distribution of the frequently and always categories combined. In both charts, the general distribution in clear, but more detail is shown with the smaller bin size. Here we can see the most common range of proportions (between 70% and 75%), the normal distribution, the range, and where the bell curve lies along the proportion values. Because this data was collected from a likert scale question, combining and showing the frequently and always categories may allow for more accurate interpretation. It is understood that the remaining proportion reported sometimes or less in mask wearing frequency. By essentially comparing 2 categories of mask wearing reports (sometimes/rarely/never and frequently/always), more focus is put on the general mask wearing practices rather than becoming distracted by the differences between all 5 original categories. **Best choice of idiom:** In this case, I would use this histogram with the larger bins to provide the clearest picture of the distribution. As discussed, comparing all 5 frequency categories is distracting and misleading. However, the histogram implies comparison between sometimes/rarely/never and frequently/always. The larger binned histogram provides enough detail while still being easily read. If the distribution were not normal, I would have recommended the ECDF, but, in this case, the histogram has the most important benefits of the ECDF and more.

### ECDF

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/1c.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/1c.png*

This ECDF also displays the combined proportions who frequently or always wear a mask. Here the x-axis has the proportions, and the y-axis has the cumulative distribution of the number of counties. The consistent increase reveals a lack of clusters and the normal distribution. This idiom makes it easy to draw quick conclusions about the mask wearing practices of counties. For instance, it can be seen that about 20% of counties reported less than 60% prevalence of frequently or always wearing masks. This information could also be used to determine the proportion greater than or between two values. We can also see the overall range of the distribution as well as the lower quartile, median, and upper quartile. With this data, I do not think easily seeing these key statistics is very valuable.

## Part 2 - US Census Bureau County Population dataset

### Boxplot

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/2b.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/2b.png*

On initial creation, the boxplot seemed almost useless. It was clear that there is a major skew to the right, but the quartiles are completely unreadable due to that extreme skew. To fix this, I added `{clip: true}` to the second boxplot which allowed me to reduce the displayed domain from 0-40,000,000 to 0-200,000 without removing any data. Removing data in this case would have an impact on the distribution and would not be a responsible choice because the extreme values are likely not false data values, just highly populated areas. Therefore, the second boxplot is just a zoomed in version of the first boxplot. Beyond the skew, together the charts show the outliers, quartiles, median, and the minimum and maximum values and the tooltip reveals the exact values of these statistics. Unfortunately, the skew means both versions of the boxplot are needed, the original and the zoomed view. Just showing the zoomed version would be misleading.

### Histograms

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/2h.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/2h.png*

The skew also had a major impact on the histogram. The first histogram has bins of 500,000 and shows the full range of data from a population of 0 to 40,000,000. This chart again provides very little information other than the skew. The second chart has the same bin size but is zoomed in to only show the data for counties whose population is less than 1,000,000. This chart provides even less information. However, by changing the bin size to 20,000 while in this zoomed in version, more detail begins to emerge. The most common bin value in this last chart is 0 to 20,000 with the number of counties in each bin decreasing with each population increase. Again, just displaying this last chart without a note about the values not included would not allow for an interpretation of the full distribution. Therefore, this still is not a good fit for displaying this data. 

### ECDF

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/2c.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/2c.png*

A similar technique of the zoom is used for the ECDF to provide some extra readability. The use of the cumulative distribution on the y-axis as well as the total number of counties being put in the subtitle help not lead viewers to a poor interpretation. The skew is still obvious, but we can also find the quartiles and median more easily as well as determine the percent of counties less than, more than, or between certain population values, especially if a tooltip were added. Without the tooltip, it is more challenging to find values because of the distance from the x-axis. It can be seen that about 89% of counties have a population of less than 200,000. **Best choice of idiom:** This is zoomed in ECDF is clearly the most useful chart for this data. The skewed nature of the distribution makes the other idioms very difficult to interpret, but the ECDF handles this well.

## Part 3 - US Census Bureau County Population dataset

### Boxplot

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/3b.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/3b.png*

In this boxplot, the 2019 birth rates, death rates, and net migration are displayed. The axis values for the birth rate and death rate are kept the same (0 to 40) for comparison purposes. Due to the different nature of the net migration data, I did not decide to put all three on the same aligned scale since comparing key statistics between all three would not be relevant. Here we can compare death and birth rates in terms of key statistics. For instance, one can easily see that the median birth rate is slightly higher than death rate and that death rate has a larger overall range. It can also be concluded that the median net migration rate is close to zero and the largest net migration rate is near 125. Boxplots with multiple glyphs are most useful for comparison. However, the net migration cannot and should not be compared with the birth and death rates. Therefore, this would be a great choice of idiom if net migration were not included.

### Histograms

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/3h.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/3h.png*

Both histograms show the distribution of the birth rates of the counties. The first one has a bin width of 3 while the second one has a bin width of 1. The histogram with a bin width of 3 does not provide enough detail for the tightly distributed data. The smaller bins also allow for more precise conclusions to be drawn about most common ranges of birth rates as well as the maximum and minimum values. Here we can see that between 10 and 12% is the most common range with the distribution quickly decreases on either side. The only issue with this graph is in the decreased ability to do quick calculations considering the large range of the number of counties per bin. However, this idiom does allow for clear interpretation of the general distribution.

### ECDF

![My chart here.](https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/3c.png)
*URL: https://github.com/cs625-datavis-fall20/hw5-distributions-McKaylaHagerty/blob/master/3c.png*

Here the x-axis has the birth rate, and the y-axis has the cumulative distribution of the number of counties. The ECDF for birth rates shows that the distribution is normal. Likewise, the steep slope especially between 9% and 13% birth rate conveys the tight distribution. We can make quick calculations and the percentages of counties is easier to work with than the counts. I could also find the key statistics but also get more valuable information than easily interpreted from the boxplot. For instance, I can see that about 30% of counties reported a birth rate of less than 10%. A tooltip would be very useful here as well. Without it, the tight distribution makes it difficult to pull out key values. **Best choice of idiom:** Again, the ECDF is what I would choose to display the data. Its shape reveals the normal nature of the distribution and the cumulative distribution percentages are easier to work with when dealing with the large number of counties.  

## References
 
1. [Linear Regression with Skewed Data](https://www.kaggle.com/c/grupo-bimbo-inventory-demand/discussion/21585)
