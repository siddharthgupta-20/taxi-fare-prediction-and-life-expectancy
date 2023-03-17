# life-expectancy
Importing necessary library

● Reading the file

● Removing the null values

● Finding the correlation matrix

● Plotting the correlation matrix using plotly and seaborn

● This metric is very helpful in understanding the relation between the features as high
correlation implies highly related. we can see (infant_death,under-5 death),
(GDP,percentage expenditure),(thinnes 1-19 years,thinness 5-9 years) these are some
which have high correlation. This can also be seen intuitively as in each tuple the
mentioned parameters are almost similar in nature.

● Plotting histogram for life expectancy. This shows that the average life expectancy is
between 70 to 80 years

● we see that in developing nations the mortality is present below 70 years as well but in
developed nations the mortality is zero below 50 in this dataset.

● Calculation of RFECV was not working for me(it kept on running without giving any
output. There might be many reasons for it may be my data is not cleaned enough,
maybe there are way too many parameters and I tried to shrink it into very small values).

● Scaling the data using the standardScaler().(all calculations will be done on this dataset).

● Converted the Country and status columns into labels for better computation.(strings can
not be passed into the models.)

● Splitting the data.

● Applying linear regression with K fold validation(almost similar to part 1,some small
changes based on the requirements)

● Applied lasso regression with cross validation and finding the best fit

● Applied Rigg regression with cross validation and finding the best fit.

● Applying pseudo inverse method as well.
