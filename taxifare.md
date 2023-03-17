# taxi-fare-prediction

● Import files using the kaggle.json file that is, using the kaggle API to download the data
and extracting it.
● importing necessary library. We import some library later in the code as per our use.

Cleaning DATA:
● Removing all the null values then resetting the index
● Checking and removing the negative value of fare amount
● Removing the latitude and longitude according to the facts(latitude extend from -90 to 90
and longitude extend from -180 to 180
● Removing very small value of fare amount from the dataset.
● Removing datapoints which have very large value of passengers taking only 6
passengers at max.
● New york coordinates are around 41-latitude to (-73)- longitude so removing the data
points far away from these coordinates range(40 - 42 and -73 to -75)
● Also some of the latitude and longitude value were exchanged which i replaced back in
the dataset as well

Pre-processing:
● Finding correlation between various parameters with the fare amount to see which
relates with the fare.
● Converting the date-time into the readable format
● Scaling the data and plotting various graphs like fare vs Haversine distance, fare vs
passenger count, fare vs day of week ,etc.
● I also plot manhattan distance against the fare to observe the output, it also showed that
there is high relation between the distance and fare amount which is expected.

Models:
● Linear regression:
Cross validation with user defined K and self implemented.
First I created my own linear regression model using sklearn library and the
converted it into k fold cross validation where I split the data into k parts then splitting the
data into training and test and finally calculating the score.
(everything is done on scaled data)
● Pseudo inverse:
np.dot(np.dot(np.linalg.inv(np.dot(A.transpose(),A)),A.transpose()),y_tra
in)
This is the algorithm to calculate the weight vector. Here A is the numpy matrix of the
inputs. The error is quite low in this (~0.01) hence it is a good metric to calculate our
outcome.
I tried to create K fold validation for pseudo inverse as well but a “UFuncTypeError” pop
up which i was unable to resolve for a very long time(~8 hours) I also tried to use sympy
which uses symbols for all calculations but still could not resolve the error.
● I also tried to use a support vector machine for it. But it returns only labels so we have to
convert out y_train to a label (using labelEncoder()) but still it wasn’t good enough hence
i choose not to show it and comment it out.
Finally I created a pipeline for scaling training and validating the data.
