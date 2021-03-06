# Kepler Exoplanet Search Results
10000 exoplanet candidates examined by the Kepler Space Observatory. Anywhay, what are exoplanets? What are exoplanets? Exoplanets are planets beyond our own solar system. Thousands have been discovered in the past two decades, mostly with NASA’s Kepler Space Telescope.

These exoplanets come in a huge variety of sizes and orbits. Some are gigantic planets hugging close to their parent stars; others are icy, some rocky. NASA and other agencies are looking for a special kind of planet: one that’s the same size as Earth, orbiting a sun-like star in the habitable zone.

The habitable zone is the area around a star where it is not too hot and not too cold for liquid water to exist on the surface of surrounding planets. Imagine if Earth was where Pluto is. The Sun would be barely visible (about the size of a pea) and Earth’s ocean and much of its atmosphere would freeze.


# Context
The Kepler Space Observatory is a NASA-build satellite that was launched in 2009. The telescope is dedicated to searching for exoplanets in star systems besides our own, with the ultimate goal of possibly finding other habitable planets besides our own. The original mission ended in 2013 due to mechanical failures, but the telescope has nevertheless been functional since 2014 on a "K2" extended mission.

Kepler had verified 1284 new exoplanets as of May 2016. As of October 2017 there are over 3000 confirmed exoplanets total (using all detection methods, including ground-based ones). The telescope is still active and continues to collect new data on its extended mission.

Content
This dataset is a cumulative record of all observed Kepler "objects of interest" — basically, all of the approximately 10,000 exoplanet candidates Kepler has taken observations on.

This dataset has an extensive data dictionary, which can be accessed here on [NASA](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html). Highlightable columns of note are:
1. kepoi_name: A KOI is a target identified by the Kepler Project that displays at least one transit-like sequence within Kepler time-series photometry that appears to be of astrophysical origin and initially consistent with a planetary transit hypothesis
kepler_name: [These names] are intended to clearly indicate a class of objects that have been confirmed or validated as planets—a step up from the planet candidate designation.
2. koi_disposition: The disposition in the literature towards this exoplanet candidate. One of CANDIDATE, FALSE POSITIVE, NOT DISPOSITIONED or CONFIRMED.
3. koi_pdisposition: The disposition Kepler data analysis has towards this exoplanet candidate. One of FALSE POSITIVE, NOT DISPOSITIONED, and CANDIDATE.
4. koi_score: A value between 0 and 1 that indicates the confidence in the KOI disposition. For CANDIDATEs, a higher value indicates more confidence in its disposition, while for FALSE POSITIVEs, a higher value indicates less confidence in that disposition.

As for the scope of this analysis, some columns have been omitted. You can find the original Kaggle dataset here on [Kaggle](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

![Image](https://github.com/AliceSartori/Exoplanet_NASA_MachineLEarningModel/blob/main/exoplanets.jpeg)


# Classifier algos used
1. Neural Network & Deep Learning
2. Random Forest classifier
3. GridSearchCV on Random Forest, a method that evaluates all combinations I define in my list of params. 

# Is Accuracy the best metric?
To not incurr in an imbalanced classification problem (a scenario where the number of observations belonging to one class is significantly lower than those belonging to the other classes), I used classification report to get recall, precision and F1 score.

In fact, the predictive model developed using conventional machine learning algorithms could be biased and inaccurate.

This happens because Machine Learning Algorithms are usually designed to improve accuracy by reducing the error. Thus, they do not take into account the class distribution / proportion or balance of classes.

After looking at the reports, I can say that Random Forest performs the best. With GridSearch, I wasn't able to get better results even adjusting the params. I'll investigate into these further.



