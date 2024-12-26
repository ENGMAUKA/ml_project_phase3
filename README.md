# ml_project_phase3
Machine Learning Classification Problem

# **1. Overview**
Tanzania, a developing nation, faces challenges in supplying its more than 57,000,000 inhabitants with water that is safe for drinking. It is extremely difficult for people to find clean, sanitary water if they do not reside close to one of the three large lakes that border the country, as one-third of the country is arid to semi-arid. Consequently, Tanzanians rely heavily on groundwater as their primary supply of water;


According to the Sustainable Development Goals (SDG) standards, just 61% of Tanzanian households presently have access to a basic water supply, 32% to basic sanitation, and 48% to basic hygiene. As a direct result, Tanzania has had to deal with mortality and illness, with the poor and vulnerable, women, and children bearing the brunt of this burden. Inadequate WASH services are thought to be the cause of 31,000 fatalities annually in Tanzania, accounting for almost 10% of avoidable deaths. These deaths also cost the country more than $2.4 billion annually in lost productivity and additional medical expenses.

The nation already has a large number of water points (stations), but some of them require maintenance, while others have completely failed.

The project aims to builds classification model, using an iterative approach, to predict the condition of water wells in Tanzania. The dataset for modelling was obtained from data provided by Taarifa and the Tanzanian Ministry of water. 

# **2. Business and Data Understanding**
## **2.1 Business Problem**
Victoria Inc. has been procured by the Government of Tanzania on a consultancy basis to study the severe water crisis experienced by the country and propose a data driven solution to clean water accessibility. Victoria Inc. is tasked with coming up with a  model that predicts the operating condition of the water points. This model will assist the government to:
- Prioritize maintenance and repairs based on operating status;
- Understand the failure rate of the water points;
- Optimize allocation of resources to restore the water points.  

The objective of Victoria Inc is to:
- Develop a predictive model for classifying water points;
- Identify factors that affect water points functionality; 

Proposed Solution:
- Develop a machine learning classification model with an accuracy score of 80%.

Performance Metrics:
- Accuracy
- Precision
- Recall
- F1-score

**model iterations**
- Dummy Model
- Logistic Regression
- Decision Tree
- Random Forest

## **2.2 Data Understanding**
###  **2.2.1 Data Source**
The dataset employed in the study was downloaded from https://www.drivendata.org/competitions/7/data/

The target variable has three possible values:
- **functional** - the waterpoint is operational and there are no repairs needed
- **functional needs repair** - the waterpoint is operational, but needs repairs
- **non functional** - the waterpoint is not operational

## **2.3 Methodology**
The adopted structure for the project was CRISP-DM that entails undertaking Business Understanding; Data Understanding; Data Preparation; Data Cleaning and Explanatory Data Analysis(EDA); Modelling; Conclusion and Recommendations.

# **3.Data Cleaning and EDA**

The following columns contain either similar or duplicated data, therefore, in order to avoid multicollinearity one or both of the columns will be dropped:
- *scheme_management *and *management*;
- *extraction_type*, *extraction_type_group* and *extraction_type_class*;
- *payment* and *payment_type*;
- *water_quality* and *quality_group*
- *quantity* and *quantity_group*
- *source* and *source_type*

![alt text](image.png)
54.2% of the water points are functional, 38.8% are non functional while the remaininig 7% are functional but needs repair.

![alt text](image-1.png)

![alt text](image-2.png)

Quantity_group_enough, waterpoint_type_other, extraction_type_class_other, construction_year and amount_tsh are the most important features.

# **5. Conclusion and Recommendation**
Random Forests was the best performing model with Decision Tree being the second best model. The poor performance of the Logistic Regression models indicate that the data is not easily separable. The Random forest model performs with an 78% testing accuracy and precision for the functional class at 81%. It also had the highest f1 score of any model at 82%.

The main source of water for Tanzania is ground water. There are a high number of functional water points Iringa, Shinyanga, Kilimanjaro, Arusha,  Morogoro and Pwani regions. The regions of Mbeya, Lindi, Rukwa, Tabora and Mara have a higher number of non function pumps water points. Therefore, more resources should be allocated to these areas as the situation is critical. There is a cluster of functional but need repair water points in Lake Victoria, Southern Coast, Lake Rukwa,  Pnangani and Lake Tanganyika basins. These should be addressed to prevent failure which can be more expensive to repair.

The Random Forest model showed that the most important features are quantity of water (enough), water point type and extraction type for the waterpoint. There are over 8,000 waterpoints that have enough water in them but are non functional. These are recommended as high priority class to address. Wells with no fees are more likely to be non functional. Payment provides incentive and means to keep wells functional. Water points managed by VMC, WUG and Water Board have a lower rate of pump failure. The three organizations can be used for case studies on good water point management practices. Investigate why these installers have such a high rate of failure or use other installers.

Future work for this project involve improving the quality of the data moving forward as well as using different model classifiers to compare performance. Better data trained in our model will improve the predictions. 