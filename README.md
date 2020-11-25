# DORIANforPredictingChronologicalAge-AoTOC

    Machine Learning Models 
FIRST DATASET PREPROCESSING:
The first step after having an idea about the biological features for the DORIAN mice is to have a good look at the data shape and make a decision on what to take as a baseline. Since the main concept of our project is to figure out the health-span and Aging process, it becomes essential to focus on the mice's age and the mother's diet while pregnant (keeping in mind the data is token for their children), focusing mainly on the wild type. 
SECOND FEATURES ENGINEERING:
The next step will be by handling the features taking a good step to:
Find out features correlation and acceptance.
Find out the best features to have a good prediction accuracy.
The main idea is to take the Age as the class label so we have 3 different class labels holding the mouse age (3, 12, 18 months).
the first run will be by predicting the mouse age through the lab measurements, taking all 75 features (with continuous values )
I replaced each age of (3, 12, 18 months) to be (1, 2, 3)
1 = 3 months
2 = 12 months
3 = 18 months
It’s necessary to say that there is:
3 months = 215
12 months = 173
18 months = 186

I added (diet) to the dataset as a feature.
Another replacement held for the diet feature replacing (cd, hfd) to be (0,1)
0= cd (controlled diet)
1 = hfd (high fat diet)
Now I will split the dataset to be 2 (training and testing), this step is important since we need to check the classifier accuracy in order to make sure whether the model can make a good prediction. Where the test.csv does not contain the class label (age), and the train.csv holds all features values plus the (age) column.
Train file = 474 mouse (with redundant values )
Test file =  100 mouse (with redundant values)

The main file consists of (575row x 76column)
Missing Data Treatment
The missing values filled using the mean_value function, every cell filled with its column mean value.
