# yahoo-fantasy-hockey-pool
We construct a NN regression model to optimize hockey yahoo fantasy points. To do so, we consider two models:
* A minimal model based on https://pub.towardsai.net/how-to-win-your-nhl-pool-without-even-trying-42bc03b9659; we neglect height/weight, add relevant Yahoo Fantasy stats (see Hypothesis section), and we identify player positions as a binary statement: Defensemen (0) or Forward (1)
* An advanced model which includes advanced stats

Each analysis notebook examines predictions with respect to points per game (PPG) and fantasy points per game (FPPG). Like Gobeil's article, we neglect goaltenders since their stats are completely different.

# Files
1. hockey-reference_scraper.ipynb : https://www.hockey-reference.com scraper
2. data_processing.ipynb : notebook used to clean, process and prepare data for analysis with respect to both models described above.
3. minimal_model_analysis.ipynb : analysis of the minimal model
4. adv_model_analysis.ipynb : analysis of the advanced model
5. all_data_*_v* : training and test data (years 2008 to 2020). Used in analysis notebooks
6. all_data_*_test : stats from the 2021 season used to predict 2022 outcomes. Used in analysis notebooks

Files used for data_processing and the scraper are not available at the moment. 

# Motivation
Advanced stats are frequently used to assess a player's performance. As an non-expert, it is unclear to me how predictive weight such metrics carry in regard to fantasy pools. To be concrete, we consider Yahoo Fanasy and apply the Express Settings: https://hockey.fantasysports.yahoo.com/hockey/express_settings?type=point.

# Goal
1. Determine the impact of advanced stats to PPG production.
2. Determine the impact of advanced stats to Yahoo FPPG production. 

# Hypothesis
1. Based on Gobeil's model, PPG appears to be well-modelled by a linear model with stats from two previous sesons. We therefore expect advanced stats to merely finely tune the results yielding small improvements at best, or worst behaviour depending on the dataset size.
2. Yahoo FPPG depends on other stats namely +/-, PIM, PPP, and SG. Such stats could be influenced by some advanced stats such as "Shots Through %", Power Play advanced analytics, and normalized +/-. It is therefore conceivable that we observe larger departures from the PPG regression task.
