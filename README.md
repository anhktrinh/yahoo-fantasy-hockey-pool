# yahoo-fantasy-hockey-pool
We construct a NN regression model to optimize hockey yahoo fantasy points. To do so, we consider two models:
* A minimal model based on https://pub.towardsai.net/how-to-win-your-nhl-pool-without-even-trying-42bc03b9659
* An advanced model which includes advanced stats

# Files
1. hockey-reference_scraper.ipynb : https://www.hockey-reference.com scrape
2. data_processing.ipynb : notebook used to clean, process and prepare data for analysis with respect to both models described above.
3. minimal_model_analysis.ipynb : analysis of the minimal model
4. adv_model_analysis.ipynb : analysis of the advanced model
5. all_data_*_v* : training and test data (years 2008 to 2020). Used in analysis notebooks
6. all_data_*_test : target data for predicting 2022 outcomes. Used in analysis notebooks

Files used for data_processing and the scraper are not available at the moment. 
