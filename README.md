# cs412_machine_learning_project
Project Overview

In this project, we focused on understanding, classifying, and predicting various entities based on their characteristics. The work involved multiple steps, including data exploration, classification, and regression modeling, to draw insights and make accurate predictions. Below is a breakdown of the process.

** Data Collection and Exploration

We began by examining the provided datasets to understand their structure and content. The datasets included labels for different entities (e.g., fashion, health, travel) and numerical values for prediction purposes. The exploration phase allowed us to:

+Identify key categories within the data.
+Analyze trends and relationships between variables.
+Recognize patterns that informed the classification and regression models.

**Classification Tasks

+Objective:

The classification task aimed to categorize entities into predefined categories such as Fashion, Tech, Health and Lifestyle, etc.


Process:

+Data Preprocessing: Cleaned and prepared the data for modeling. This included handling missing values and standardizing features.

+Model Training: Developed and trained classification models using algorithms like logistic regression or decision trees to assign labels to entities.

+Evaluation: Assessed model accuracy using metrics such as precision, recall, and F1 score. Adjustments were made to improve performance in subsequent rounds.

Outcomes:
Entities were successfully categorized into relevant classes, improving our understanding of their industry or sector association.

** Regression Tasks

+Objective:
The regression task focused on predicting numerical outcomes based on available features.

Process:

+Feature Engineering: Selected relevant features that could influence predictions. This step involved removing irrelevant or noisy data.
+Model Training: Built regression models (e.g., linear regression, random forest) to predict numerical outcomes, such as engagement metrics.
+Optimization: Refined the models by tuning hyperparameters and validating with test data to enhance accuracy.
Outcomes:
The regression models effectively predicted values like engagement rates, enabling more precise forecasting and planning.

** Iterative Refinement
Throughout the project, we adopted an iterative approach:

+Each round of classification or regression involved learning from errors and improving model performance.
+Insights from one phase informed the next, leading to better results over time.


** Challenges and Resolutions

+Data Imbalance: Some categories were underrepresented. We addressed this through oversampling and adjusting class weights in models.
+Overfitting: To ensure generalization, we used techniques like cross-validation and regularization.
+Complexity in Relationships: Nonlinear relationships were handled using advanced algorithms like ensemble methods.
**********************                    **********************                      **********************                   **********************             **********************

#ROUND 1 Classification
In the first round, the main task was to classify Instagram accounts into one of the predefined categories, such as Fashion, Travel, Tech, Health and Lifestyle, and others.

Process:

+Data Analysis:

We examined the data to understand the distribution of categories. The dataset showed that some categories were larger than others, creating an imbalance.
+Model Development:

We used a basic machine learning classification algorithm to assign each account to a category based on its features. These features included metadata such as account descriptions and recent posts.

+Evaluation:

After training the model, we tested its performance using accuracy as the main metric. We also identified categories that were more difficult to predict, such as those with fewer examples.

+Outcome:

The model performed reasonably well, especially in popular categories like Fashion and Health and Lifestyle. However, less common categories like Art and Mom and Children had lower accuracy. This showed us the need for better balancing or feature selection in future rounds.

#ROUND 1 Regression

The regression task focused on predicting the number of likes (like_count) for posts from the accounts.

Process:

+Data Preparation:
We noticed that the like counts had a heavy-tailed distribution, meaning a few accounts had extremely high likes while most had moderate or low likes. To address this, we used the log transformation of like counts for modeling.
+Model Development:
A basic regression model was developed to predict like_count based on features like engagement metrics, content type, and account popularity.
Validation:
We evaluated the model using Mean Squared Error (MSE) to measure how close the predictions were to the actual values.
+Outcome:
The model captured general trends but struggled with extreme cases (e.g., very high or very low like counts). This was a learning point for handling outliers and improving feature selection in the next round.

+Challenges:
Data Imbalance:
Some categories had much less data than others, making it harder for the model to learn them effectively.
Skewed Data:
Like counts were highly skewed, which affected regression performance, especially for extreme values.

**********************                    **********************                      **********************                   **********************             **********************
#ROUND 2 Classification

In Round 2, our primary focus for classification was to assign entities (e.g., accounts, profiles) to one of the predefined categories such as Tech, Fashion, Food, and others.

Process:

+Data Preparation: We carefully examined the classification data to address any imbalances between categories. This step ensured that all categories had enough examples for the model to learn effectively.
+Feature Engineering: We selected key features, such as account descriptions and post content, to improve the predictive power of the model.
+Model Selection and Training: We used a supervised classification algorithm, optimizing it for accuracy. The categories included diverse and overlapping labels, so tuning the model was critical.
+Evaluation and Refinement: After training, we tested the model on the provided test set and iteratively refined it based on performance metrics.
+Outcome:
The model achieved good accuracy, especially in categories like Tech, Fashion, and Health and Lifestyle. However, some overlapping labels (e.g., between Entertainment and Art) showed room for improvement. The adjustments made in this round contributed to a more balanced performance.

#ROUND 2 Regression

regression task aimed to predict numerical outcomes, specifically the popularity of content (e.g., likes, engagement levels).

Process:

+Understanding the Data: We analyzed the provided numerical data and observed trends such as the distribution of like counts, which showed a heavy-tailed pattern.
+Model Development: We developed a regression model that included both linear and nonlinear relationships to predict like_count.
+Addressing Challenges: To manage outliers and skewed distributions, we applied techniques like log transformation of the target variable.
+Validation: The model was validated using Mean Squared Error (MSE) as the evaluation metric.
+Outcome:
The predictions were more reliable than in the first round, particularly for accounts with moderate popularity. For extremely high or low engagement, the predictions showed minor inconsistencies, likely due to the variability in content style.

+Improvements in Round 2:
Enhanced data balancing for better classification performance.
Addressed outliers and variability in regression tasks using more advanced preprocessing techniques.
Improved overall accuracy and consistency of models compared to Round 1.

**********************                    **********************                      **********************                   **********************             **********************

#ROUND3 Classification

In Round 3, we focused on refining our classification model to categorize Instagram accounts into predefined groups like Tech, Fashion, Food, and Travel. The aim was to improve accuracy and handle complex cases more effectively.

Process:

+Data Refinement:

Cleaned and rechecked the data to ensure there were no errors or inconsistencies.
Balanced the categories by increasing the representation of smaller groups, such as Art and Mom and Children.
Feature Optimization:
Selected the most meaningful features, such as account descriptions, post types, and hashtags, to improve the model’s understanding.
Removed irrelevant or noisy data that could affect predictions.

+Model Adjustment:

Fine-tuned the classification model using advanced hyperparameter tuning.
Tested multiple algorithms and selected the best-performing one for the final predictions.
Evaluation:
Used metrics like precision, recall, and F1 score to measure performance.
Focused on reducing errors in categories with overlapping features, like Entertainment and Art.

+Outcome:
The final classification model showed significant improvement, especially in handling smaller or complex categories. It achieved the highest accuracy across all rounds, can correctly identifying almost all accounts correctly.

#ROUND3 Regression

The regression task 3 aimed to predict the popularity of posts (like_count) on a log-transformed scale to reduce skewness and improve prediction accuracy.

Process:

+Advanced Feature Engineering:
Included additional variables, such as engagement rates, follower counts, and content type (e.g., video, image).
Transformed like_count with log scaling to address extreme values and better model the data.

+Model Refinement:
Experimented with ensemble methods (e.g., random forest regression) to capture nonlinear relationships.
Applied cross-validation to ensure the model generalized well on unseen data.
Outlier Handling:
Identified and adjusted for outliers in the data that could heavily influence the model.
Evaluation:
Evaluated the model using Mean Squared Error (MSE) on log-transformed like_count.
Focused on reducing errors in predictions for highly popular or niche accounts.

+Outcome:
The regression model in Round 3 achieved much better accuracy compared to earlier rounds. It handled both high and low engagement levels more consistently. The overall performance was solidly built and reliable.









