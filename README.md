# DataCleaningCarPrices
Im using CarPrices that i downloaded on kaggle, because the dataset already good, i must broke some of the data so i can start cleaning it... once it was cleaned.. i start to predict another prices using LinearRegreesion

i start with broke the csv and then i continue to fix it, first i make all the types become one (float),
to do that all the string, and null value will be converted into NaN using errors = "coerce"

then i try to find the median of the each column that i will use to fill NaN
after that the independent variabel will be clean enough.

now about the dependent variabel which is price... i cant use median value because it is dependent of another variables, i also cant use median in case if there are outliers inside the database (True)

so i start to use ML - Linear Regression instead to predict the null value, i start to input 
the independent and dependent variabels, after i done that.. i wanna see the entire dataset so i
df.to_csv named testCarPrice

then about the outliers, im using IQR.. in order to know how much the upper and lower bound
once i got them, i start to change the outliers with the upper and lower value or winzorising
and then now the data has been cleaned perfectly (i guess) and ready to be predict new data

to predict new price i need the regression one... so i start use linear regression as my model... 
i make the minimum X so user wont put much input. there a some bug (maybe?) my data arent have NaN but when i start to run... the error said i has.. but when i check it use x.dtypes, there is no NaN so
i use simple imputer to fill the nan, after that it works.. i made the test size 40% with random 22
then put the new data into column and start to predict...

the last one is evaluation... im using MSE,MAE and RMSE
