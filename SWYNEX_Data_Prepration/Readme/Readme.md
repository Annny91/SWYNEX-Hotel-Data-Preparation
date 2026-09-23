## Task 1: Data Preparation



#### Project Overview:



This project focuses on preparing a public hotel booking dataset for reliable downstream data analysis and machine learning.



The dataset contains historical booking records for a city hotel and a resort hotel. It includes information about booking timing, stay duration, guest counts, booking channels, customer type, room information, pricing, cancellation status, and reservation status.



The original public dataset contains 1,19,390 booking records and 32 variables. The source describes hotel demand data from a resort hotel and a city hotel, covering bookings due to arrive between July 2015 and August 2017.



## &#x20;  **Business Context**



Imagine a hotel group has provided historical booking data and wants to use it for future analysis of booking behaviour and cancellation patterns.



Before performing analysis or building a predictive model, the raw data needs to be checked and prepared.



The purpose of this task is therefore to transform the raw dataset into a cleaner and more reliable dataset that can be used for future analysis.



&#x20;  Task Objective



The main objectives of this task are:



\* Inspect the dataset structure

\* Identify missing values

\* Handle missing values based on their business meaning

\* Check and correct data types

\* Identify duplicate records

\* Check suspicious or invalid values

\* Validate the prepared dataset

\* Document data preparation assumptions

\* Export a cleaned dataset





#### Dataset: Hotel Booking Demand Dataset



The dataset contains booking information for:



\* Resort Hotel

\* City Hotel



##### Important fields include:



\* Hotel type

\* Cancellation status

\* Lead time

\* Arrival date information

\* Length of stay

\* Number of adults, children and babies

\* Meal type

\* Country

\* Market segment

\* Distribution channel

\* Deposit type

\* Customer type

\* Average daily rate

\* Special requests

\* Reservation status

\* Reservation status date



#### Tools Used



\* Python

\* Pandas

\* NumPy

\* Jupyter Notebook

\* VS Code

\* GitHub



#### Data Preparation Performed



##### &#x20;   1. Data Inspection



The raw dataset was inspected for:



\* Number of rows and columns

\* Column names

\* Data types

\* Basic statistical information

\* Unique categorical values



##### &#x20;   2. Missing Values



Missing values were investigated column by column.



The following decisions were made:



\* `children`: missing values were treated as 0

\* `country`: missing values were labelled as `Unknown`

\* `agent`: missing values were retained as missing because an artificial agent ID should not be created

\* `company`: missing values were retained as missing because an artificial company ID should not be created



##### &#x20;   3. Data Types



Data types were reviewed according to the meaning of each field.



Examples:



\* Booking counts and flags were maintained as numeric/integer fields

\* `adr` was maintained as a numeric field

\* Categorical fields were maintained as text/string fields

\* `reservation\_status\_date` was converted to a proper datetime type



##### &#x20;   4. Duplicate Records



Exact duplicate rows were identified and removed.



Only complete duplicate records were removed. Records were not considered duplicates simply because they shared individual field values.



##### &#x20;   5. Data Quality Checks



The project checks for:



\* Negative lead times

\* Negative average daily rates

\* Invalid cancellation flags

\* Invalid guest counts

\* Zero-guest bookings

\* Remaining duplicate records

\* Remaining missing values

#### 

#### &#x20;  Assumptions



The main assumptions are documented inside the notebook.



The most important assumptions are:



1\. Missing `children` values represent zero children.

2\. Missing `country` values are labelled `Unknown` instead of guessing a country.

3\. Missing agent/company identifiers are not replaced with artificial IDs.

4\. Exact duplicate rows are removed.

5\. Negative values in logically non-negative fields are treated as data-quality issues.

6\. The raw dataset is preserved and all transformations are performed on a working copy.

7\. This task is limited to data preparation and does not make business or predictive conclusions.



#### &#x20;  Project Structure



SWYNEX\_Data\_Prepration/

│

├── data/

│   └── hotel\_bookings.csv

│

├── notebook/

│   └── 01\_data\_preparation.ipynb

│

├── output/

│   └── hotel\_bookings\_cleaned.csv

│

└── README.md





&#x20;  Output



The main output of this task is:



`output/hotel\_bookings\_cleaned.csv`



The cleaned dataset is intended to serve as the input for future exploratory analysis and machine learning tasks.





Possible next stages of the project include:



\* Exploratory Data Analysis

\* Cancellation pattern analysis

\* Feature engineering

\* Data visualization

\* Cancellation prediction

\* Model evaluation



