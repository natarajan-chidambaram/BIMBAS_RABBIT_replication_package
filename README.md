# BIMBAS_RABBIT_replication_package

This repository provides the replication package used for developing BIMBAS. 
BIMBAS stands for Bot Identification Model Based on Activity Sequences. This is a binary classification model to identify bot accounts based on their recent activities on GitHub. This is the model that is used in RABBIT to identify bots in GitHub.    
RABBIT is a recursive acronym for "RABBIT is an Activity-Based Bot Identification Tool". RABBIT is quite efficient, being able to predict thousands of accounts per hour, without reaching GitHub's imposed hourly API rate limit of 5,000 queries per hour for authorised users.    

BIMBAS has been developed by Natarajan Chidambaram, a researcher at the [Software Engineering Lab](http://informatique.umons.ac.be/genlog/) of the [University of Mons](https://www.umons.ac.be) (Belgium) as part of his PhD research in the context of [DigitalWallonia4.AI research project ARIAC (grant number 2010235)](https://www.digitalwallonia.be/ia/) and [TRAIL](https://trail.ac/en/).   

BIMBAS was developed as part of the research article titled: "A Bot Identification Model and Tool based on GitHub Activity Sequences" that is submitted to the Journal of Systems and Software. 

1. notebooks/Grid_search.ipynb - A Jupyter notebook used for identifying the classification model (classifier + hyperparameters) that can detect bots in GitHub based on their activity sequences.
2. notebooks/Eliminating_features.ipynb - A Jupyter notebook used for eliminating the features (from the initial set of 45 features) that do not contribute to the performance of the classification model. The combination of results obtained in (1) and (2) led to BIMBAS.
3. notebooks/BIMBAS_evaluation.ipynb - A Jupyter notebook used for evaluating BIMBAS on unseen data, identify the top most important features that BIMBAS uses for decision-making.
4. data/train_feat.csv - A csv file that provides the list of contributors and the features based on activity sequences that were used for training BIMBAS.
5. data/train_label.csv - A csv file that provides the labels for the contributors in (4)
6. data/test_feat.csv - A csv file that provides the list of contributors and the features based on activity sequences that were used for evaluating BIMBAS in unseen data.
7. data/test_label.csv - A csv file that provides the labels for the contributors in (6)
