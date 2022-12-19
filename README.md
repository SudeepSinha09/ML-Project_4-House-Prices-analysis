# ML-Project_4-House-Prices-analysis
### Data Details 

  Kaggle - https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data?select=train.csv  
  Colab Notebook - https://colab.research.google.com/drive/1FZTPoNwGMCGACbwx48rblvQ1SqgPXFn_?usp=sharing
  
#### Please use the Ipynb file in the repository for a detailed explanation of this project. This is because the project has been completed and the steps have been written in the notebook referenced in the repository.
Link - https://github.com/SudeepSinha09/ML-Project_4-House-Prices-analysis/blob/main/House%20Prices%20analysis.ipynb

## Description

![image](https://user-images.githubusercontent.com/93086122/208372919-da0021b0-88eb-4dec-a1b5-929642605847.png)

Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

## An Overview of EDA

![image](https://user-images.githubusercontent.com/93086122/208373193-3ded2f0e-a1d5-4522-bd95-00d5afba2dea.png)

![image](https://user-images.githubusercontent.com/93086122/208373723-5e89f71f-7692-4c22-87bb-b74ee814983b.png)

![image](https://user-images.githubusercontent.com/93086122/208373765-f43087ce-ebe5-40bf-8322-93a03e9deb19.png)

### Dataset Description

#### File descriptions
  train.csv - the training set  
  test.csv - the test set  
  data_description.txt - full description of each column, originally prepared by Dean De Cock but lightly edited to match the column names used here  
  sample_submission.csv - a benchmark submission from a linear regression on year and month of sale, lot square footage, and number of bedrooms  

## Project Brief

First I have done Data preprocessing In data preprocessing

I've imported libraries
Then imported datasets both train and test Data
have done data cleaning via removing null values from train data and test data

To remove null values I've used the standard procedure of removing the columns with more the 50% null values and for columns having less than 50% null values will be handled by the below methods Add columns mean to numerical columns Add columns mode to categorical columns

After doing the above procedure for both train and test data I've done some data visualization using sns and plotted heat plot

After this dealing with categorical variables have been done In this process, the categorical variables were labeled using dummy regressor

After doing this I've done test train split of the training data

After doing the test train split I've Build some models using

Multiple linear regression
Random forest regression
XGBoost regression
After using these regressions I've compared the r^2 values for the best model selection

After comparing the r^2 value I've done Hyperparameter tuning using RandomizedCV

The best model (random forest regression) is been selected for further calculations

Now I've predicted the output using the above model

And answered the question above attached CSV file format

#### Data fields

Here's a brief version of what you'll find in the data description file.

SalePrice - the property's sale price in dollars. This is the target variable that you're trying to predict.  
MSSubClass: The building class  
MSZoning: The general zoning classification  
LotFrontage: Linear feet of street connected to property  
LotArea: Lot size in square feet  
Street: Type of road access  
Alley: Type of alley access  
LotShape: General shape of property  
LandContour: Flatness of the property  
Utilities: Type of utilities available  
LotConfig: Lot configuration  
LandSlope: Slope of property  
Neighborhood: Physical locations within Ames city limits  
Condition1: Proximity to main road or railroad  
Condition2: Proximity to main road or railroad (if a second is present)  
BldgType: Type of dwelling  
HouseStyle: Style of dwelling  
OverallQual: Overall material and finish quality  
OverallCond: Overall condition rating  
YearBuilt: Original construction date  
YearRemodAdd: Remodel date  
RoofStyle: Type of roof  
RoofMatl: Roof material  
Exterior1st: Exterior covering on house  
Exterior2nd: Exterior covering on house (if more than one material)  
MasVnrType: Masonry veneer type  
MasVnrArea: Masonry veneer area in square feet  
ExterQual: Exterior material quality  
ExterCond: Present condition of the material on the exterior  
Foundation: Type of foundation  
BsmtQual: Height of the basement  
BsmtCond: General condition of the basement  
BsmtExposure: Walkout or garden level basement walls  
BsmtFinType1: Quality of basement finished area  
BsmtFinSF1: Type 1 finished square feet  
BsmtFinType2: Quality of second finished area (if present)  
BsmtFinSF2: Type 2 finished square feet  
BsmtUnfSF: Unfinished square feet of basement area  
TotalBsmtSF: Total square feet of basement area  
Heating: Type of heating  
HeatingQC: Heating quality and condition  
CentralAir: Central air conditioning  
Electrical: Electrical system  
1stFlrSF: First Floor square feet  
2ndFlrSF: Second floor square feet  
LowQualFinSF: Low quality finished square feet (all floors)  
GrLivArea: Above grade (ground) living area square feet  
BsmtFullBath: Basement full bathrooms  
BsmtHalfBath: Basement half bathrooms  
FullBath: Full bathrooms above grade  
HalfBath: Half baths above grade  
Bedroom: Number of bedrooms above basement level  
Kitchen: Number of kitchens  
KitchenQual: Kitchen quality  
TotRmsAbvGrd: Total rooms above grade (does not include bathrooms)  
Functional: Home functionality rating  
Fireplaces: Number of fireplaces  
FireplaceQu: Fireplace quality  
GarageType: Garage location  
GarageYrBlt: Year garage was built  
GarageFinish: Interior finish of the garage  
GarageCars: Size of garage in car capacity  
GarageArea: Size of garage in square feet  
GarageQual: Garage quality  
GarageCond: Garage condition  
PavedDrive: Paved driveway  
WoodDeckSF: Wood deck area in square feet  
OpenPorchSF: Open porch area in square feet  
EnclosedPorch: Enclosed porch area in square feet  
3SsnPorch: Three season porch area in square feet  
ScreenPorch: Screen porch area in square feet  
PoolArea: Pool area in square feet  
PoolQC: Pool quality  
Fence: Fence quality  
MiscFeature: Miscellaneous feature not covered in other categories  
MiscVal: $Value of miscellaneous feature  
MoSold: Month Sold  
YrSold: Year Sold  
SaleType: Type of sale  
SaleCondition: Condition of sale  
