# M.Tech-Project

In this project we mainly want to retreive some information from a large datasets in very less time. This is the objective of our project.
DATASET USED
Our datasets consists of electricity consumption data from december 201 to june 2018 from residential building inside IIT Bombay campus. The building consists of 39 apartments, each having a smart meter and logging data at an interval of 5 seconds. The data we will be using in project is downscaled at 1 hour interval. We have 39 CSVs file each of an apartment. The header in CSV are 
1.Timestamp
2.V1 - voltage of phase 1
3.V2 - voltage of phase 2
4.V3 - voltage of phase 3
5.w1 - power consumption of phase 1
6.w2 - power consumption of phase 2
7.w3 - power consumption of phase 3

PROPOSED SYSTEM
we will be using pyspark to implement spark framework. Whole project is implemented in google colab. CSV files are uploded on colab. We perform different operation on each file by passing their file path. After passing file path of a csv we will create a dataframe of that csv. The most important column in dataframe is timestamp. This is a unique number which always change. This entity will work as a primary key in our project. We will pass any date from december 2016 to june 2018 and that time will be converted to timestamp. Using that timestamp as a primary key and applying filter query we will find out power consumed on that particular date. In this project we are using spark due to its in memory computation feature which will help in reducing the time of fetching and searching data.
