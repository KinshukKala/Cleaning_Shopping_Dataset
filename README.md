# Shopping Dataset Cleaning and Exploration

## Objective

The objective of this project is to perform basic data cleaning and exploration using Python and Pandas.

## Dataset

The dataset used in this project is the Shopping Dataset available on Kaggle:

https://www.kaggle.com/datasets/anvitkumar/shopping-dataset

## Tasks Performed

- Loaded dataset into Pandas DataFrame
  
- Explored data using:
  - head()
  - tail()
  - info()
  - describe()
    
- Handled missing values
  - Replaced by median value for numerical feature(discount)
  - Replaced by NA for categorical features(seller_name, seller_information, what_customers_said)
  - Dropped columns variations and videos as they had too many missing values

- Removed unnecessary columns:
  - images:  Contains image URLs and is not usable for ML models. 
  - videos: Contains video URLs and has a high percentage of missing values. 
  - variations: More than half of the values were missing and the column was not essential for analysis. 
  - amount_of_stars: Provides information same as rating and ratings_count. 
  - breadcrumbs: Contains nested category-path information that overlaps with the category column. 
  - best_offer: Mostly contains {} values and contains information already given by discount and final_price. 
  - more_offers: Contains information already given by discount and final_price. 
  - currency: Contains only a single value (INR) and therefore provides no additional information.
    
- Performed row filtering

- Checked for duplicate rows
 
- Created derived features:
  - quantity: Random values between 1 and 10.
  - total_amount: total_amount = quantity * final_price
  
- Saved cleaned dataset

## Files

- Combined_dataset.csv : Original dataset
- cleaned_dataset.csv : Cleaned dataset
- ShoppingDatasetCleaning.ipynb : Jupyter Notebook
- README.md : Project summary
- requirements.txt : Libraries & tools

## Libraries Used

- Pandas
- NumPy

## Author

Kinshuk Kala
