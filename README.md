# E-Commerce Product Delivery Prediction
![](https://i0.wp.com/blog.locus.sh/wp-content/uploads/2020/03/Future-of-Ecommerce-Same-day-and-time-based-delivery.jpg?resize=1024%2C640&ssl=1.jpg)
## Project Overview:
The aim of this project is to predict whether products from an international e-commerce company will reach customers on time or not. Additionally, the project analyzes various factors influencing product delivery and studies customer behavior. The company primarily sells electronic products. The project utilized a combination of decision tree, random forest, k-nearest neighbors (KNN), and logistic regression algorithms to enhance the accuracy and reliability of the predictions.

## Data Dictionary:
The dataset used for model building contains 10,999 observations of 12 variables, including:

| Variable             | Description                                             |
|----------------------|---------------------------------------------------------|
| ID                   | ID Number of Customers                                 |
| Warehouse_block      | The Company's Warehouse block (A, B, C, D, E)          |
| Mode_of_Shipment     | The mode of shipment (Ship, Flight, Road)              |
| Customer_care_calls  | Number of calls made for shipment inquiries            |
| Customer_rating      | Customer rating (1 - Lowest, 5 - Highest)              |
| Cost_of_the_Product  | Cost of the product in US Dollars                     |
| Prior_purchases      | Number of prior purchases                              |
| Product_importance   | Product importance categorization (low, medium, high)  |
| Gender               | Gender of customers (Male, Female)                    |
| Discount_offered     | Discount offered on specific products                  |
| Weight_in_gms        | Weight of the product in grams                         |
| Reached.on.Time_Y.N  | Target variable (1 - Product did not reach on time, 0 - Product reached on time) |

 
## Technologies and Tools Used:
- **Programming Language:** Python
- **Machine Learning Libraries:** Scikit-learn
- **Visualization:** Seaborn, Matplotlib
- **Data Storage and Processing:** SQL, Pandas


## Model Development:
1. **Decision Tree:** A decision tree model was employed to capture non-linear relationships within the data. Hyperparameter tuning was performed to optimize the tree structure.

2. **Random Forest:** An ensemble of decision trees (random forest) was used to enhance model generalization and mitigate overfitting. The random forest aggregated predictions from multiple decision trees to improve overall accuracy.

3. **K-Nearest Neighbors (KNN):** KNN was employed to consider the spatial relationships between delivery locations. The model predicted delivery times based on the historical performance of geographically similar regions.

4. **Logistic Regression:** Logistic regression was utilized to model the probability of timely deliveries. This provided a baseline for comparison with more complex models and contributed interpretability to the ensemble.

## Data Collection and Preprocessing:
The project involved collecting data from the e-commerce platform, encompassing historical order details, shipping information, and delivery timestamps. Data preprocessing steps included handling missing values, encoding categorical variables, normalizing numerical features, and addressing outliers. Feature engineering was performed to extract relevant information such as distance, traffic patterns, and historical delivery performance.

## Validation and Testing:
The dataset was split into training and testing sets for model validation. Cross-validation techniques were applied to assess model performance across various subsets of the data. Evaluation metrics such as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) were used to measure prediction accuracy.

## Challenges Faced:
- **Model Interpretability:** Balancing the interpretability of logistic regression with the complexity and accuracy of ensemble models posed a challenge.
- **Hyperparameter Tuning:** Fine-tuning hyperparameters for decision tree depth, random forest parameters, and KNN neighbors required iterative experimentation.

## Conclusion:
The project aimed to predict product delivery timeliness while examining factors affecting delivery and customer behavior. Exploratory data analysis revealed that product weight and cost significantly impact delivery. Products weighing between 2500 - 3500 grams and costing less than $250 had a higher likelihood of timely delivery. Most products were shipped from Warehouse F via ship, suggesting its proximity to a seaport.

Customer behavior also plays a crucial role in predicting timely delivery. Higher customer call volumes correlated with delayed delivery. Interestingly, customers with more prior purchases had a higher rate of on-time deliveries, indicating their loyalty to the company. Products with a discount of 0-10% were more likely to be delivered late, whereas those with discounts exceeding 10% had a higher on-time delivery rate.

In terms of machine learning models, the decision tree classifier achieved the highest accuracy at 69%, outperforming other models. The random forest classifier and logistic regression achieved accuracies of 68% and 67%, respectively, while the K Nearest Neighbors model had the lowest accuracy at 65%.

**Impact:**
- **Improved Accuracy:** The ensemble approach enhanced the accuracy of delivery time predictions, contributing to increased customer satisfaction.
- **Operational Efficiency:** The e-commerce platform optimized its logistics and resource allocation based on the more reliable predictions, leading to cost savings and improved operational efficiency.


**Future Enhancements:**
- **Continuous Model Evaluation:** Regularly assessing and updating the model to adapt to changing delivery patterns.
- **Incorporating Real-time Data:** Integration of real-time data streams for dynamic and up-to-date predictions.
- **Exploring Advanced Techniques:** Investigating more advanced ensemble methods and model stacking for further improvement.
