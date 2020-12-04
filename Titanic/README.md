This is a README file for Titanic data analysis.
This is an Exploratory Data Analysis project where the aim is to design a model to predict the survival of passengers in the titanic based on the attribites given in train.csv dataset.
The dataset is taken from the kaggle website.
In order to build a model, preprocessing of data (train and test) was done as follows:
1. "Sex" = {'female','male'}. COnverting categorical attributes into integers .. i.e., female: 0, male:1
2. "Age" : handling the missing values by replacing it with the avergae age by gender
3.  "embarked": segregated into 3 columns as  "embarked_c","embarked_Q" & "embarked_S" using pd.get_dummies()
4. Dropping ['Name','Ticket','Cabin'] columns
5. "Fare" : converting float type to int type

Final data attributes with few records:  

        PassengerId  Survived  Pclass  Sex   Age  SibSp  Parch    Fare  Embarked_C   Embarked_Q  Embarked_S  
0            1         0       3    0        22.0      1      0     7           0     0           1  
1            2         1       1    1        38.0      1      0    71           1     0           0  
2            3         1       3    1        26.0      0      0     7           0     0           1  
3            4         1       1    1        35.0      1      0    53           0     0           1
4            5         0       3    0        35.0      0      0     8           0     0           1

         


Building a model:
Divided the train.csv into X_train and Y_train
X_train: Drop PassengerID and Survived columns
Y_train: only has Survived columns
build a model to fit X_train and Y_train
X_test: 'Test.csv' with droping PassengerID
test the model built with X_test and calculate the accuracy.

I built logistic regression model using X_train and Y_train. 
When tested the model with Y_test, the accurary came to 80.47%

