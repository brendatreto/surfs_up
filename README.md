# Surfs Up

## Overview

The purpose of this analysis is to retrieve information about temperature trends to make an informed decision before opening a surf shop. The information was stored in an SQLite database. Potential investors are interested in the idea but have some valid concerns, especially related to the weather conditions. 

To answer his questions and ease the investors' concerns we will provide statistical analysis of the weather trends.

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

We saved these results in a list and created DataFrame to perform the statistical analysis and got the following outcomes:

**Fig 1. Statistics for the months of June and December**

![june_temp](https://user-images.githubusercontent.com/22451540/155758079-dc4378e0-fd86-4371-a1be-6905976f101c.PNG) ![dec_temp](https://user-images.githubusercontent.com/22451540/155758154-5a933ac1-86f5-4fd8-bd65-4900bc837a7a.PNG)

Three main differences are noteworthy:
1. The average temperature has a variation of around 3 degrees (74.9°F in June vs 71.4°F in December)
2. The minimum temperatures have a greater variation, as was expected (64°F in June vs 56°F in December). A difference that can have an impact on the behavior of potential customers.
3. There is only a slight difference in the maximum temperatures (85°F in June vs 83°F in December. This might not represent a challenge, on the contrary, it works as an indicator of stability for the business.

## Summary
Looking at the information presented above we can confidently say that the differences in temperature are important to take into consideration. The differences might not affect behavior significantly, so the business opportunity seems solid, but further analysis is needed.
- Investors should consider precipitation trends for the months of June and December since this might also have a significant effect on the behaviors of customers.
- Consider filtering information by stations. There might be significant differences among these, and could be used in favor of making the best decision.
