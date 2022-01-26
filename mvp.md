## Hit and runs in Chicago -- MVP
### Ryan Solava

This project seeks to predict conditions in Chicago under which hit and run crashes are most likely to occur. Hit and runs are on the rise in the city, and they represent a large percentage of fatal crashes. After some initial analysis, there does seem to be several features that could help predict if an accident was a hit and run. The figure below shows how the percentage of crashes varies with the time of day for all crashes and for hit and runs.

![Percentage of crashes by time of day](time_of_day.png)

Both categories are most frequent in the afternoon hours, during rush hour, but hit and runs are much more likely to occur at night. A decision tree trained on the latitude, longitude, hour, day of week, month, and posted speed limit achieved an f1-score of .60. This score can likely be improved by including other features, doing feature engineer, using other models, and handling class imbalance. I would also like to consider soft classifiers and examine the ROC curves for them. Soft classification is particularly interesting for this problem, since having a score that indicates if a hit and run is likely, is more useful than a simple yes/no answer.
