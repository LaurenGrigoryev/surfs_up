# surfs_up

## Overview of the Analysis
The purpose of this analysis was to give a potential surf shop owner more information about temperature trends for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Results
* The weather statistics for Oahu were fairly similar for June and December with temperatures averaging in the 70s and highs reaching the 80s. It should be noted that the data for June might be a little more accurate as there were 1,700 observations for June and only 1,517 for December.

* In June, the mean temperature is about 75, a great temperature for ice cream and surfing, as seen in this June statistics summary.

* In December, the mean temperature is 71, which is still not too cold to deter ice cream eaters and surfers. Here is a December statistics summary. 

## Summary
Having analyzed the data, I would advise keeping the shop open year-round as the weather in Oahu is similar in June and December with highs in the 80s and lows not dipping past 56 in December and 64 in June. The standard deviation is between 3 and 4 points for both months, which is a good indication that most days do in fact feel like the mean temperatures.

I would suggest performing at least two more queries before finalizing a plan. Rain could easily drive away business. I would suggesting finding precipitation levels and averages for the two months by running these queries:

1) June_Rain = []
   June_Rain = session.query(Measurement.prcp).filter(extract('month', Measurement.date)==6).all()
   
2) December_Rain = []
   December_Rain = session.query(Measurement.prcp).filter(extract('month', Measurement.date)==12).all()

