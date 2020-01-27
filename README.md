# Seattle_Terry_Stops
Analysis of Seattle Terry Stop data set, and a classification model for predicting an arrest.

The file `Coronet_Consultants_Seattle_Terry_Stops.pdf` contains the presentation for the projectr. It summarizes the main findings and recemmended next steps.

The Python notebooks are in the directory `notebooks`. A short description of the notebooks in this directory is given below:

1) `data_exploration.ipynb`: This notebook analyzes the Terry Stop data to get a sense for the data we are dealing with. It was the first notebook we created

2) `log_reg_part_2.ipynb`:

3) `logistic_regression.ipynb`: This notebook runs the scorecard model on the data with added features. It contains a third degree polynomial scorecard on 4 features: `Officer Gender`, `Reported Time`, `weapon_present`, and `Initial Call Type`. The most important feature for the model is `Initial Call Type`. The accuracy of the model is 71% (AUC = 86%). Note that a naive version would score around 97 % accuracy. So, this is not a very successful model. Also note that the trarget is the physical arrest.

4) `model_new_target.ipynb`: 

5) `trees.ipynb`: This notebook implements a decision tree in a scorecard for the physical arrest target. The achieved accuracy is 91 %. Better than a scorecard based on logistic regression alone, but still well below a naive implementation by predicting no arrest which will achieve an accuracy of around 97 %.

6) `umap_model.ipynb`:

The data files are in the sub-directory `data`.

1) `Terry_Stops_added_features.csv`: The same as `Terry_Stops_raw.csv` data set but augmnented with features. 

2) `Terry_Stops_raw.csv`: The original data setr that we used for the project. The data (including a desc ription of the fields) can be found at https://catalog.data.gov/dataset/terry-stops

3) `subset.csv`: (unsure...)

