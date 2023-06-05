# analysis_of_the_AAB_test
**Product** - a mobile application for food delivery.

**Research objective** - to study the behavior of mobile application users.

**Tasks:**
- Study and verify the data
- Analyze the sales funnel to understand how users make purchases
- Investigate the results of an A/A/B experiment on font changes

**Data description:**
- EventName - event name
- DeviceIDHash - unique user identifier
- EventTimestamp - event time
- ExpId - experiment number: 246 and 247 are control groups, and 248 is the experimental group.

**Сontents:**
- Data preparation
- Data exploration and verification
- Let's examine the results of the experiment
- Output

**Conclusion**

During data preprocessing, duplicates were removed, missing values were checked, and data types were changed where necessary. Also, columns were renamed for convenience. The following conclusions were drawn during data analysis:

There were 243,713 events and 7,551 users in the log. On average, each user had 20 events. The majority of events occurred from August 1-7, so data for this period was removed, and a new data frame was created. 2826 events and 17 users were lost during data validation. Both A/B test groups had approximately 80,000 users each.

The event funnel was examined, and the following event sequence was created:
- Visiting the main page
- Visiting the offer page
- Adding to cart
- Successful order placement
- 
There were 5 types of events in the log, but one of them was very rare, so it was removed and did not make it into the funnel. This event was related to user training and occurred only 1018 times, which is very low compared to other events. It is also important to note that 98.5% of users visit the main page, 60% visit the offer page, 49% reach the cart page, and only 46% complete a successful payment. The biggest drop-off in user engagement occurs between the main page and the offer page. Only 47.7% of users make it from the first to the last step of the funnel.

An A/A/B test analysis was conducted.

Each group had approximately 2,500 unique users.

It was also found that the two control groups (246 and 247) did not differ at any level of significance (0.05 and 0.1). This means that the groups produced the same results.

The most popular event was visiting the main screen: 2450 visits for group 246 and 2476 visits for group 247.

Next, the control groups were compared to the experimental group. All tests found no difference between the groups.

To ensure accuracy, the two control groups were combined into one and compared to the test group. Here too, the test group showed the same result as before changing the fonts.

Based on the entire study, it can be concluded that font changes are not necessary, as they do not have any impact. Other growth points should be explored instead.
