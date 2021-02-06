# Divvy'in Up Data

## 📝 Project Description
This project analyzes anonymized data from Divvy, a rideshare biking service in Chicago, IL. We chose to examine data in the third quarter of 2019 which includes the summer months and high volume of riders compared to other quarters. Our analysis examines relationships between gender, age, yearly subscribers and one-off customers, in addition to popular routes, bikes, and stations.


## 🔎 Questions to Answer
We wanted to uncover interesting patterns in the data. We asked ourselves:
* Are there routes and stations that are more popular than others?
* Are there any specific bikes that were rented a surprising amount?
* Are there any relationships between the age and/or gender when comparing one-time customers or yearly subscribers?
* How long, on average, are trips made by Divvy bike?


## 📊 Observations
### Popular Stations
* The most popular station by far is Streeter Dr. and Grand Ave. which is located on Navy Pier. It is a popular destination for both tourists and locals. Indeed, this station appeared as either the starting or ending station on many of the most popular routes.

### Popular Routes
* All of the most frequented routes were in the loop and along the lakefront. Without knowing, we suspect that this is again a combination of tourists and commuters making use of the bikes in downtown Chicago.

### Subscribers vs Customers:
* 84% of riders during this time frame were yearly subscribers rather than riders who pay for one-off rides. 
* This data may be skewed. We made an early call to drop any data with null values. We suspect that the dropped cells are more likely to be customers, one-time or infrequent users.

### Gender:
* There are far more male Divvy riders than female - about 70% to 30%.
* It is fairly the same gender breakdown when it comes to customer (about 70/30) and subscriber (about 60/40).
* Divvy did not collect gender data beyond male and female, which means portions of Chicago's non-binary population are not accounted for in this dataset.

### Age:
* Riders aged 20-29 made up 47% of overall ridership with people aged 30-39 coming in second with 30% of overall ridership. 
* The breakdown per usertype, customer versus subscriber, was similar to the overall categories. 


 ## 🧼 Data Cleanup Summary
 * **Age:** Divvy only provided the birthyear of users, not their current age so we added a quick calculation to get their age in 2019 based on birth year provided. Once we had the ages converted, we grouped and binned those into groups for easier analysis. 
 * **Gender:** We noticed that the gender column contained many null values so we decided to drop them. That reduced our dataset of 1.6 million rows to 1.3 million rows. As noted in our analysis, we suspect this impacts the accuracy of analysis on both customer data and the gender breakdown. 
 * **Trip Duration:** The original dataset includes start time, end time, and trip duration. Once we started analyzing trip duration, it became clear that the original data didn't make sense. Even if it was being counted in seconds or milliseconds, it didn't correlate to the difference in minutes. We manually created a new column calculate the difference between start and end time in minutes. 


## 📁 Repository Contents
| Title | Description |
| --- | --- |
| **Main Repository** |
| Divvy'ing Up Data Final Notebook | The complete Jupyter Notebook file with all relevant data analysis. |
| Data Exploration and Cleanup Process | A walkthrough of our data cleanup and exploration process. |
| Divvy Presentation Final | A PDF version of our slideshow presentation. |
| **Resources** |
| Divvy Trips 2019 Q3 | The csv file containing our dataset.|
| **Images** | PNG versions of all visuals generated in our data analysis. |


## 💻 Contributors:
* Charlie Denys
* Nabila Farooqi
* Ruth Hinkle
* Drew McBride
* Andrew Nehrer