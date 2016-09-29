# PUI2016_oa691-HW3_oa691
This repo is for HW-3 Assignment 1, 2 and 3

Assignment-1:  
Problem Statement: Write an ipython notebook that demonstrates visually in a data-driven way the central limit theorem. Plot all sample means, generate distributions as histograms, describe behaviour in terms of law of large numbers.

Given: 
Sample size : 100
Population: N>10 & N< 2000
Iteration Range: 1-100
Assume same mean for all distributions = 100
Statistical Distributions Methods: Normal, Poisson, Binomial, Chi-Squared and logistic

Solution Approach:
Using the  ipython notebook on jupyter and following the code instructions provided, I imported pylab, numpy and matplotlib. I created a list of distrubution names to which I continually referred to set the statistical functions. I then created an empty dictionary md {} and passed into it an array of values from the data set. 

I used the docs.scipy site to find out about numpy random distributions types. I then defined parameters for each distribution type and calculated the mean and standard deviation sigma and plotted. 

To show the central limit theorem, I created a list of 99 integers of random numbers between 10 and 2000. I then provided ipython with a for loop to draw random samples. Inside another for loop, I calculated the means of the distributions. I then scatter-plotted sample size for the distribution and its means. A histogram for each calculation is also plotted to show the number of occurances in each sample.

Conclusion:  
Increasing the iterations of statistical calculation on sample of a population leads to the actual means' convergence to the theoretical mean. The of large numbers states that as the number of trials increase, the calculated results will converge over to the guess number. Mean 100 is the guess value. The scattered plot, in poisson distribution for example, show that the actual mean converges to the theoretical 100 as more interations are performed.

Scattered plots also shows that as more distribution calculations are made, the shape of that distribution becomes a normal distribution
as stated by the central limit therom. This can be oberved on all the distributions. The range of extreme means may change but the curve becomes normal to x-axis with each iteration nonetheless. 

A close inspection on the binomial will show that the convergant mean number with this distribution has remained at 90 even though I defined the theoretical mean to be 100 in my code. This may be due the float parameter, p. The p parameter must be between 0 and 1 and for this practice I defined as 0.9. When I experimented with p, I noticed that as I increased p to 0.999, the means' distribution became closer to ~100. This may indicate that with binomial means are dependent on the sample size and also the precision of the sampling.

Sources: https://github.com/fedhere/PUI2016_fb55/blob/master/HW3_fb55/Assignment1.ipynb
http://docs.scipy.org/doc/numpy/reference/generated/numpy.random.binomial.html

Assignment-2:

Problem Statement: 
Set up the work for data-driven inference based on CitiBike data. Define the idea and the hypothesis.
 
Question: Do subscriber bikers ride more frequently than those who have not subscribed to citybike

Hypothesis: Customers who have a membership to citybike use citybikes significantly more in a given month. 

Null Hypothesis:
The usage of citybikes among members is the same or lower in a given month than the usage who do not have the membership.

Alternative Hypothesis:
The usage of citybikes is significantly higher among customers with membership. 

Confidence/significance Level:
Confidence level is 95%. and the significance level is 5%, alpha = 0.05.

Given: 
raw city bike 02/2015 usage data set 

Solution Approach:    
While preparing this homework assignment I studied with Kelsey, Matt, Marc, and also with Bailey who contrinuted to the groups' collaboration through emails.

Before the start of the data analysis, as a group we discussed an idea. Initially, as a first idea, I recommended the comparison of citybike riders born after 1990 to those born before. However, to keep the analyis simple, we as the group instead decided to study citybike usage between subscribers and those riders who are not members.

I followed the code instructions and imported ipython functions, created a datestring and assigned the february 2015 of the citybike data to that string. 

Using the import zipfile function, suggested by Kelsey and Bailey, I unzipped the citybike file located on the URL link. This data is then assigned to the object dataframe df to display it as a spreadsheet on the notebook. To return and display all the rows of data I used the df.head().

Moving forward, I used df.columns to display the column titles. This allowed me to see how the table columns are organized and remove the ones I wanted to drop from the list by using df.drop([]) and a boolean true/false method. I then rendered the data again only returning usertype for february.

As I tried to plot, ipython gave me errors. Based on this error and instructions for assigment-2 where it said to set == the male and female and seperate them, I realized that the substring needed to be changed to integers. At this point, I followed Kelsey's method to  assign 1 to subscribers and 2 to customers, and also her method for test and display of the column for the usertype-subscriber. Based on the suggestion from Matt and Marc to clearly display the large data I defined limits to the y-axis with higher value.    

Conclusion:
This plot is the bar chart type plot of the chosen data frame. We can not attest to the null or alternative hypothesis at this point but we can only compare the usage and conclude that the highest citybike rides occurred on Wednesdays during February 2015 and that the subscribed members used it much more frequently than those other customers, approximately 40000 to about 1000. 


Sources: 
https://github.com/fedhere/PUI2016_fb55/blob/master/HW3_fb55/citibikes_gender.ipynb
http://stackoverflow.com/questions/17142304/replace-string-value-in-entire-dataframe
