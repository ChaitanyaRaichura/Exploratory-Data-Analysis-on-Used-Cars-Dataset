# **Exploratory Data Analysis (EDA) of Used Cars Dataset from Craigslist.org**

_**Data Analysis**_ or sometimes referred to as _**exploratory data analysis (EDA)**_ is one of the core components of data science. This repository represents data analysis and its visualization using _**python**_ and its libraries such as _**Pandas, NumPy, Matplotlib**_ and _**Seaborn**_. For this purpose [_Used Cars Dataset_](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) dataset has been taken from _**Kaggle**_.


## **Dataset Overview**

- The dataset is taken from Kaggle and contains details of the _**used cars in USA**_ which are listed on _**Craigslist.org**_. It contains large collection of used vehicles for sale divided into _**26 different columns**_ and around _**0.42 million records**_ in it.
- The dataset is not clean and hence a lot of cleaning is carried out and then further analysis and visualization is done on it.
- The analysis is divided into two separate jupyter notebook namely [_Cleaning_raw_data.ipynb_](Cleaning_raw_data.ipynb) and [_Analysis_of_used_cars_dataset.ipynb_](Analysis_of_used_cars_dataset.ipynb).
- The data cleaned using [_Cleaning_raw_data.ipynb_](Cleaning_raw_data.ipynb) is stored as [_clean_data.csv_](clean_data.csv) and after further improvisation using [_Analysis_of_used_cars_dataset.ipynb_](Analysis_of_used_cars_dataset.ipynb) it is stored as [_final_clean_data.csv_](final_clean_data.csv).

## **More Information**

- The raw data stored in [_vehicles.csv_](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) is extracted from [_Cars_dataset_compressed.zip_](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) file.
- The raw data in [_vehicles.csv_](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) is used in [_Cleaning_raw_data.ipynb_](Cleaning_raw_data.ipynb) for exploring, cleaning, analysing and visualizing.
- The csv file [_vehicles.csv_](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) is included in .gitignore as it is a huge sized file and it can also be extracted from [_Cars_dataset_compressed.zip_](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) file.

## **[Cleaning_raw_data.ipynb](Cleaning_raw_data.ipynb)**

It starts with extracting some basic information about data in [_vehicles.csv_](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data) and includes further steps such as:
- Dropping unnecessary columns.
- Checking for missing values and taking actions accordingly as per the requirement of each column separately and providing some extra _**data wrangling**_ to get genuine results.
- Looking for _**outliers**_ in _**YEAR**_ and _**PRICE**_ columns using _**boxplots**_ and removing them using some _**statistical operations**_. Also plotting of boxplots after removing outliers in both the columns to see the changes accordingly.
- Output in boxplots before and after removing outliers clearly shows the importance of cleaning the dataset.
- Final results of an analysis in [_Cleaning_raw_data.ipynb_](Cleaning_raw_data.ipynb) can be seen in [_clean_data.csv_](clean_data.csv). And this file will be used for further analysis in [_Analysis_of_used_cars_dataset.ipynb_](Analysis_of_used_cars_dataset.ipynb).

## **[Analysis_of_used_cars_dataset.ipynb](Analysis_of_used_cars_dataset.ipynb)**

As we continue our analysis with [_clean_data.csv_](clean_data.csv), we start with checking for duplicated rows and dropping duplicated rows and columns which are not required for further analysis. Then we move to analysis, visualization and conclusion part.

## Analysis and Conclusion:

### 1. Analysis based on year of registration of vehicle:
- _**Countplot**_ on _**year**_ of registration concludes that year _**2018 has the maximum cars registered**_ followed by year _**2017**_ and also trend shows _**most cars registered**_ are in years _**between 2013 and 2018**_.
- _**Barplot**_ of _**year of registration vs price**_ shows that _**maximum**_ price is of the vehicles which were registered in year _**2020**_ followed by _**2019**_. There is a clear _**uptrend from year 2011 to year 2020**_ in terms of average prices of vehicles.
- The _**regplot**_ between _**price and year of registration**_ shows the clear _**correlation**_ between year of registration and price of vehicles.
### 2. Analysis based on state of vehicle:
- _**Catplot**_ of _**state**_ concludes that _**maximum**_ number of vehicles registered are from _**California(ca)**_ state followed by _**Florida**_.
- _**Barplot between price and state**_ shows that state _**Wisconsin(wi)**_ has vehicles with _**maximum price**_ range.
- From _**Catplot of State vs Price**_, it can be roughly assumed that states like _**California(ca)**_ and _**Florida(fl)**_ have vehicles _**distributed in whole price range almost evenly**_.
### 3. Analysis based on manufacturer of vehicle:
- _**Catplot on manufacturer**_ of vehicle shows that the _**maximum number**_ of vehicles are of manufacturer _**Ford**_ followed by _**Chevrolet**_ and _**Toyota**_. This also showcases their _**mass production abilities**_.
- _**Barplot between manufacturer and price**_ of vehicles shows that price-wise _**Tesla**_ is _**most expensive in resale market**_ followed by _**Aston-martin**_. People are _**valuing more to the Premium EV brand**_ rather than Other Premium luxury brand. _**Least**_ value is shown by _**Morgan**_ manufacturer.
- _**Barplot between manufacturer and odometer**_ readings shows that cars of manufacturer _**Pontiac, Mercury, Land-Rover and Saturn**_ are driven many _**more miles**_ before listing it for resale.
### 4. Analysis based on transmission of vehicle:
-  _**Countplot on transmission**_ of vehicles registered shows that _**maximum**_ vehicles for resale are of _**automatic transmission**_.
- _**Barplot between transmission and price**_ of vehicle shows that _**pricing**_ of vehicles with _**automatic transmission is slightly higher**_ than vehicles with manual transmission. Almost _**all type of vehicles with automatic transmission are priced higher**_ than their respective manual transmission vehicles _**except coupe**_ type of vehicle.
- Cars running with _**hybrid fuel with manual transmission are more priced**_ than with automatic transmission.
### 5. Analysis based on condition of vehicle:
- _**Maximum**_ cars registered for resale are with _**good condition**_ followed by _**excellent**_ condition.
- Cars with _**good condition are highly priced**_ than others.
### 6. Analysis based on color of vehicle:
- **Pie chart**_ shows that _**maximum**_ cars registered are of _**white color**_ followed by cars with _**black and silver color**_.
- _**White cars**_ are _**priced at top**_ followed by _**black**_ cars.
