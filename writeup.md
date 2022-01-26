## **Hit and runs in Chicago**

### Ryan Solava

#### Abstract

In this project, we use crash data from the City of Chicago to train classifiers
to predict if a crash is likely to be a hit and run. A variety of models were
trained and compared

#### Design

Hit and runs are on the rise in Chicago. The victims of hit and runs
are double victims in that they must deal with the affects of the crash, but
also bare the financial burdens themselves without another party to hold responsible.
As part of the City of Chicago's response to this situation, here in this
project we use past crash data to predict if a given context is likely to produce
a hit and run. This will be useful to city planners and police, in helping them
to best allocate resources that could prevent these occurrences.

#### Data

 * [Chicago crash data](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if) Data on all crashes in Chicago from 2017-2021 are publicly available on the city's
 data portal. There were about 581,000 crashes. Available features include

- Time and date of crash
- Longitude and latitude
- Lighting
- Weather conditions
- Road conditions
- Road type
- Traffic signal type
- Whether it was in a work zone

And many others. There are several features such as the crash type, amount of
damage, number and seriousness of injuries that are about the results of the
crash. This data was used for some initial analysis, but was not used to train
the model, since it could not be know until after a crash occurs. Our target,
whether or not a crash was a hit or run, is also available in the dataset.

* [Chicago neighborhoods](https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Neighborhoods/bbvz-uum9) Gives the location information for Chicago Neighborhoods. Not used as a feature
for our models. Useful for visualizations.

* [Chicago neighborhood median income](https://www.chicagomag.com/Chicago-Magazine/April-2006/The-Geography-of-Money/)
Used for some initial analysis, but not ultimately used as a feature.

#### Algorithms

The following soft classifiers were trained:

* Logistic regression
* K-nearest neighbors
* Decision tree
* Random forest
* Extremely random tree
* XGBoost

Naive Bayes was also considered, but since there is a mix of continuous and
binary features, it was difficult to get an effective model.

Of these models, XGBoost was the best performing with an area under the
receiver operator curve of .655. This was after hyperparameter tuning.


#### Tools


* **XGBoost*** for the XGBoost classifier
* **scikitlearn** was where all the other classifiers came from, I also used
their model selection package to tune hyperparameters.
* **Geopandas** to plot and display geographic data.
* **Sweet Viz** for initial EDA.


#### Communication

I primarily communicated my results through slides and presentation.
Also, my code and visualizations are posted to my
[personal GitHub](https://github.com/rsolava/chicago_crashes).
