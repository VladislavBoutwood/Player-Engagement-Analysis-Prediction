# Player-Engagement-Analysis-Prediction
This project involves an exploratory data analysis (EDA) and initial machine learning modeling to understand and predict player engagement levels (Low, Medium, High).

This project aims to explore and predict player engagement patterns in online gaming using a dataset containing various player behaviors and characteristics. The goal is to identify key factors influencing player engagement and build a classification model to predict whether a player will have low, medium, or high engagement.


How to Run the Project

1.  Clone the repository.
2.  Install the required libraries (e.g., pandas, numpy, matplotlib, seaborn, scikit-learn, lightgbm, catboost).
3.  Run the Jupyter Notebook (`your_notebook_name.ipynb`) to reproduce the analysis and model training.


## Dataset

The dataset used in this project is `online_gaming_behavior_dataset.csv`. It includes information such as:

*   `PlayerID`: Unique identifier for each player.
*   `Age`: Age of the player.
*   `Gender`: Gender of the player.
*   `Location`: Geographical location of the player.
*   `GameGenre`: Genre of the game played.
*   `PlayTimeHours`: Total hours of playtime.
*   `InGamePurchases`: Whether the player made in-game purchases (binary).
*   `GameDifficulty`: Difficulty level of the game.
*   `SessionsPerWeek`: Number of gaming sessions per week.
*   `AvgSessionDurationMinutes`: Average duration of gaming sessions in minutes.
*   `PlayerLevel`: Player's level in the game.
*   `AchievementsUnlocked`: Number of achievements unlocked.
*   `EngagementLevel`: The target variable, indicating the player's engagement level (Low, Medium, High).

## Methodology

The project followed these key steps:

1.  **Exploratory Data Analysis (EDA):** Analyzed the distribution of features and their relationships with the target variable (`EngagementLevel`) using various visualizations (histograms, boxplots, count plots, KDE plots) and statistical tests (ANOVA).
2.  **Feature Engineering:** Created a categorical feature for 'PlayerLevel' for initial exploration.
3.  **Data Preprocessing:** Handled categorical features by applying one-hot encoding and ordinal encoding. The target variable was label encoded. Irrelevant features like `PlayerID` and the temporary `PlayerLevel_Category` were dropped.
4.  **Data Splitting and Scaling:** Split the data into training and testing sets (80/20 split) and scaled the numerical features using `StandardScaler`.
5.  **Model Training and Evaluation:** Trained and evaluated several classification models, including:
    *   Random Forest Classifier
    *   Decision Tree Classifier
    *   KNeighbors Classifier (KNN)
    *   Support Vector Classifier (SVC)
    *   Logistic Regression
    *   Gradient Boosting Classifier
    *   LightGBM Classifier
    *   CatBoost Classifier

    Model performance was evaluated using classification reports and confusion matrices.

## Key Findings from EDA

*   Features like Age, Gender, Location, GameGenre, and PlayTimeHours showed no significant independent correlation with EngagementLevel.
*   `SessionsPerWeek` and `AvgSessionDurationMinutes` were found to have a strong positive correlation with EngagementLevel.
*   `PlayerLevel` and `AchievementsUnlocked` also showed a correlation with EngagementLevel, with higher levels and more achievements generally associated with higher engagement.

## Machine Learning Model Performance

*(You can add a summary table here comparing the performance metrics (Accuracy, Precision, Recall, F1-score) of the trained models based on your classification reports. For example:)*

| Model               | Accuracy | Precision (Weighted Avg) | Recall (Weighted Avg) | F1-Score (Weighted Avg) |
| :------------------ | :------- | :----------------------- | :-------------------- | :---------------------- |
| Random Forest       | 0.91     | 0.91                     | 0.91                  | 0.91                    |
| Decision Tree       | 0.83     | 0.83                     | 0.83                  | 0.83                    |
| KNN                 | 0.72     | 0.72                     | 0.72                  | 0.71                    |
| SVC                 | 0.89     | 0.89                     | 0.89                  | 0.89                    |
| Logistic Regression | 0.79     | 0.80                     | 0.79                  | 0.79                    |
| Gradient Boosting   | 0.91     | 0.91                     | 0.91                  | 0.91                    |
| LightGBM            | 0.91     | 0.91                     | 0.91                  | 0.91                    |
| CatBoost            | 0.92     | 0.92                     | 0.92                  | 0.92                    |

*(Update the table with the actual metrics from your model evaluations)*

Based on the initial evaluation, models like CatBoost, Random Forest, Gradient Boosting, and LightGBM show promising results in predicting player engagement levels.

On next commitment i will add:

*   Hyperparameter tuning for the best-performing models to optimize their performance.
*   Investigating other potential features or feature engineering techniques.
*   Exploring different model evaluation metrics and techniques.
*   Analyzing feature importance to understand which factors contribute most to the predictions.
