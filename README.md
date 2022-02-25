# Surfs Up

## Overview

The purpose of this analysis is to retrieve information about temperature trends in order to make an informed decision before opening up a surf shop. The information was stored in a SQLite database. Potential investors are interested in the idea but have some valid concerns, specially releated to the weather conditions. 

In order to answer his questions and ease the investor's concerns we will provide statistical analysis of the weather trends.

### Resources
Weather conditions analysis using:
- SQLite and SQLAlchemy
- Climate App using Flask
- Visual Studio Code to create Python applications 
- Jupyter Notebook

## Results

As per our first query, we looked at the temperatures for the month of June and repeated the process for the month of December:

`session.query(Measurement.date, Measurement.tobs).filter("06" == func.strftime("%m", Measurement.date))`

`session.query(Measurement.date, Measurement.tobs).filter("12" == func.strftime("%m", Measurement.date))`

We save these results in a list and created DataFrame to perform the statistical analysis and got the following outcomes:

**Fig 1. June statistics**
![june_temp](https://user-images.githubusercontent.com/22451540/155758079-dc4378e0-fd86-4371-a1be-6905976f101c.PNG)

**Fig 2. December statistics**
![dec_temp](https://user-images.githubusercontent.com/22451540/155758154-5a933ac1-86f5-4fd8-bd65-4900bc837a7a.PNG)




## Summary
