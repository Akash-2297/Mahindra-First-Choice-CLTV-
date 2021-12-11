
# Mahindra First Choice(CLTV)


Geolocation Based Customer Analysis: The idea is to explore how various factors like car make & model, time and type of service etc. vary with location. Since the servicing industry is local in nature, this kind of an analysis could possibly render some really interesting business insights. Furthermore, this analysis will enable us to formulate more concrete machine learning problems. From the data at hand it is possible to extract insights about customer behaviour especially the following questions can be addressed


# Problem Statement 1:

Identifying the ownership pattern of cars throughout the country. This also captures the problem wherein information regarding the spending patterns can be identified Expected Business Outcome: Mahindra First Choice Services will be benefited in multiple ways. Knowing the ownership pattern targeted marketing campaigns could be carried out. Knowing the spending patterns services could be suited to the particular spending pattern.
# Problem Statement 2:
Identify the type of order each state receives and present it as an interactive visualization. Expected Business Outcome: This could potentially give information about how Mahindra First Choice needs to be prepared to tackle various seasonal cases Market Segmentation: Market segmentation is the process of dividing a market of potential customers into internally homogeneous and mutually heterogeneous groups or segments, based on different characteristics captured in the data. Groups created through such a segmentation exercise many times reveal behavioral patterns which are different from generally accepted segments by the business. The exercise is broadly known as “clustering” and is aimed at finding the consumers who will respond similarly to various stimuli by detecting underlying behavior patterns. Though clustering falls under a Machine Learning problem category called unsupervised learning, which requires extensive efforts, it is possible to carry out a visual analysis in a relatively short timespan. Problem Statement:
# Pipeline
1) Data cleaning and preprocessing performed. 
2) Null Value check
3) Uniqueness check
4) Checked for Outliers, and outlier correction done accordingly.
5) Overall data science pipeline from data to results.
6) Basic Data Exploration
7) EDA
8) Univariate Analysis
9) Bi Variate Analysis
10) Clustering
11) Model Assessment based on 2 approaches as mentioned in the subsequent sections.
12) Model Selection for Classification based on ROC/AOC.
13) Model Selection for Regression based on R Square value
# Plotly Dashboard

![20211211_151051](https://user-images.githubusercontent.com/56502247/145674086-140a074b-13da-4715-a271-797ce8758f36.gif)





## EDA



## Approach 1 - CLTV Based on Recency, Frequency and Revenue

Recency – Frequency – Revenue
Data : User Id, Invoice Date and Total Value
- Recency :  Calculated by grouping unique User Ids and and their latest invoice date
- Frequency : Calculated by grouping unique User Ids and their counts
- Revenue : Calculated by grouping unique User Ids with Total Value
- Clusters : Clustered Users to get clusters for all three columns
-  Overall Score: Combined(mean) all three cluster labels to get One overall score 

## Model Selection: ROC and AUC Score 

Models	AUC Score
- Logistic Reg	0.601
- Decision Tree	1.0
- Random Forest	1.0
- Support Vector Mechanics 0.535
- KNN 	0.997


## Model Selection: Cross Validation

- Models	Cross Validation Score 
- Logistic Reg	0.48, 0.65, 0.58, 0.574, 0.572
- Decision Tree	0.587, 0.91, 1, 1, 0.56
- Random Forest	0.655, 0.925, 0.999 , 1, 0.972
- SVM	0.337, 0.476, 0.652, 0.628, 0.555
- KNN 	0.498, 0.612, 0.615, 0.729, 0.671
## Approach 2 - CLTV Based on Average Order Size ,Purchase Frequency and Life Time Value


- Data Set	Formula
- No Of Transaction	Value Counts based on Customers
- Average Order Size	Total Revenue for the Customer/No of Transactions
- Purchase Frequency	No of Transactions for that customer (from his/her first transaction) /(total number of years from the first date of transaction till 2016)
- Life Time of the customers car	Pending Life Span of the car =(200000 - Kilometers run till date) *average kilometers run per yearAssuming 200000 is the max life of the car , and 12000 Km is on an average distance travelled by a car per year in India.
- CLTV	(Average Order Size * Purchase Frequency * Life Time of the customers car )
## Insights and Recommendations

- As value from Accidents are high, Mahindra First Choice can tie up with Insurance company to help customers meet their expenses
- Common running repairs like tightening of brakes, tyre change etc can be included in the form of Quarterly or Half yearly customized packages.
- As Maharashtra and Tamil Nadu has maximum number of outsourced services, Cost benefit Analysis of outsourced services needs to be done and High value- High Count services should be incorporated in in-house services.
- Though count of cars in M.P is less, claims from insurance is high, This indicates that there can be a possibility of cars driven recklessly is more. Thus, branding of service stores at various locations with Safe driving guidelines needs to be displayed and communicated in these states(MP, TN)
- Rainy season has high service count. Pre-rain(summer) and post-rain(winter) customized maintenance packages should be planned and floated. This will help to balance load of service during each season.
- As Maruti Suzuki, M&M, Hyundai are top 3 types of make with respect to services, value added services for such type of customers should be planned.
