# Business

For full presentation, click [here.](https://github.com/riwasabri/Business/blob/master/Business%20-%20Presentation.pdf)

## **Abstract**

The Google Merchandise Store collects a large amount of data regarding its website
visitors. This large amount of data can be daunting to analyze and extracting actionable
insights to increase conversions can be difficult.

Generally, social ads platforms allow to broadly retarget website visitors or even
specific lists of customers. The data collected presents opportunities for even more
granular targeting of users across categories by for example determining different ways
of retargeting these users based on consumer profiling defined by historical
demographics and behavioral data.

The goal of this project is to act as a first step to visualize patterns and groups in the
data, paving the way to a more advanced data science solution.

## **Data**

The [data](https://www.kaggle.com/datasets/bigquery/google-analytics-sample?select=ga_sessions_20160801) consists of user data
from google analytics. It is collected on a daily basis, with each day having 1000+ rows of associated data. For the purpose
of this EDA, one day of data was analyzed.

One row of data represents the behavior of a unique visitor represented by a unique ID
on the website. Columns contain information about traffic source, geography, device,
pageviews, hits.. etc

Additionally, [geographical data](https://developers.google.com/public-data/docs/canonical/countries_csv) was collected to retrieve the coordinates of countries in the given data.

**Assumptions:**
Given that 95% of the data consists of “non repeated” customers, I only keep a
sample corresponding to the last occurrence of a customer in order to treat the data
uniformly across users.

## **Design**

**Impact Hypothesis:**

By better understanding (1) who their users are and (2) how different types of users
convert on the website, Google Merchandise Store can create more intentional
targeting and growth strategies to increase conversions.

**Preliminary EDA:**

The following dashboards allow to explore the data in more detail:
* [Dashboard 1](https://public.tableau.com/app/profile/kiwi7232/viz/ToplineMetrics/Dashboard1): Topline Metrics give an overview of trends in geography,
ecommerce actions, channel, source…etc
<img width="1083" alt="Screen Shot 2022-11-06 at 8 57 25 AM" src="https://user-images.githubusercontent.com/31965719/200174941-28a580de-96e4-421e-a600-63207ed74c3e.png">

* [Dashboard 2](https://public.tableau.com/app/profile/kiwi7232/viz/TransactorsProfile/Dashboard2): Transactors Profile goes into more detail regarding transactors exploring relationship of transactions with visit number, pageviews..etc
<img width="1081" alt="Screen Shot 2022-11-06 at 9 01 17 AM" src="https://user-images.githubusercontent.com/31965719/200175123-cc809a3a-f8bd-441c-9508-e715a35d5881.png">

* [Dashboard 3](https://public.tableau.com/app/profile/kiwi7232/viz/GoogleMerchandiseStoreE-commerceActions/EcommerceDashboard): Purchase Intent allows to understand categories purchase intent across countries.
<img width="1082" alt="Screen Shot 2022-11-06 at 9 01 27 AM" src="https://user-images.githubusercontent.com/31965719/200175127-b6e626e9-c394-41a7-9129-5464c2992b72.png">

**Data Solution Path:**

The preliminary data analysis serves as a naive approach to getting to know the data
and paves the way to potentially using unsupervised learning for customer profiling.
This would allow them to develop tailored growth strategies based on similarities
between visitors across geographies and behavior. Clustering “types of purchasers”
can allow Google to better target consumers at different stages of the purchasing
funnel.

## **Process**

**Cleaning:**
* Cleaning consisted of deleting columns that have a majority of null values
* Changing null values to the most sensical replacement
* Removing duplicates

**Feature Engineering:**
* I created dummy variables to be able to visualize categorical variables such as
e-commerce actions

**Data Exploration and Visualization:**
* Initial Aggregation and Visualization in Excel
* Preliminary EDA in tableau

## **Tools**

* Pandas for pre-processing
* Excel for Cleaning and EDA
* Tableau for EDA and visualization
