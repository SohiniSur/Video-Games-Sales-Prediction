# Video-Games-Sales-Prediction
Objective: the code aims to understand what factors influence video game sales and create models to predict future sales.
The code analyzes a video game sales dataset to understand sales trends and build predictive models.

-----------------------------------------------------------------------------------
Description: The dataset contains information about video game sales, critical reviews, and other attributes. It's often used for exploring sales trends and building predictive models.

Columns and Data Types:

Column	Description	Data Type
Name	Name of the video game	String
Platform	Platform the game was released on (e.g., PS4, Xbox One, PC)	String
Year_of_Release	Year the game was released	Integer/Numeric
Genre	Genre of the game (e.g., Action, Sports, RPG)	String
Publisher	Publisher of the game	String
NA_Sales	Sales in North America (in millions)	Numeric
EU_Sales	Sales in Europe (in millions)	Numeric
JP_Sales	Sales in Japan (in millions)	Numeric
Other_Sales	Sales in other regions (in millions)	Numeric
Global_Sales	Total worldwide sales (in millions)	Numeric
Critic_Score	Aggregate score compiled by Metacritic staff	Numeric
Critic_Count	Number of critics used in coming up with the Critic_Score	Numeric
User_Score	Score by Metacritic's subscribers	Numeric
User_Count	Number of users who gave the User_Score	Numeric
Developer	Party responsible for creating the game	String
Rating	The ESRB ratings (e.g., E for Everyone, T for Teen)	String

-----------------------------------------------------------------------------------
Process:
Data Loading and Cleaning:

Loads a video game sales dataset from a CSV file using pandas.
Handles missing values by imputing with median (for numerical) and mode (for categorical) or filling with 'Unknown'.
Removes duplicate rows.

Exploratory Data Analysis (EDA):

Visualizes the distribution of global sales using a histogram.
Identifies and plots the top 10 best-selling games.
Analyzes and plots total global sales trends over the years, by genre, and by platform.

Linear Regression Modeling:

Selects features (Critic Score, User Score, Platform, Genre) for modeling.
Creates dummy variables for categorical features (Platform, Genre) using pd.get_dummies.
Splits data into training and testing sets.
Trains a Linear Regression model.
Evaluates the model using Mean Squared Error (MSE).

CatBoost Regression Modeling:

Installs the catboost library if not already installed using !pip install catboost.
Creates and trains a CatBoost Regression model.
Specifies categorical features (Platform, Genre) for CatBoost.
Evaluates the model using MSE and R-squared.

XGBoost Regression Modeling:

Installs the xgboost library if not already installed using !pip install xgboost.
Creates and trains an XGBoost Regression model.
Evaluates the model using MSE.


--------------------------------------------------------------------------------------
Conclusion:

The analysis of the video game sales dataset reveals key insights into sales trends and the factors influencing game success. We observed that:

Sales Trends: The video game market has experienced fluctuations over the years, with specific platforms and genres driving sales at different times. Understanding these trends can inform strategic decisions for game development and marketing.
Genre and Platform Impact: Certain genres like Action and Shooter tend to be more popular and have higher global sales. Similarly, platforms such as PS2, X360, and PS3 have historically dominated the market.
Predictive Modeling: Machine learning models, especially CatBoost and XGBoost, demonstrate promising predictive capabilities for forecasting global sales based on features like critic scores, user scores, platform, and genre. While Linear Regression provides a baseline, more sophisticated models capture the complexities of the data better.
By leveraging these insights and predictive models, game developers and publishers can make more informed decisions regarding game development, platform selection, target audience, and marketing strategies to maximize their chances of success in the competitive video game market. Further analysis and model refinement could lead to even more accurate sales predictions and better strategic planning.

Market Dynamics: The video game market is constantly evolving. Continuous monitoring of emerging trends and adapting models accordingly is crucial for sustained success.
External Factors: Economic conditions, cultural shifts, and technological advancements can significantly influence sales. These factors should be considered in conjunction with the insights derived from the analysis.
Data Limitations: The dataset used has limitations, such as missing values and potential biases. Addressing these limitations and incorporating more data sources could enhance the reliability and accuracy of the findings.
By acknowledging these considerations and continuously refining the analysis, stakeholders in the video game industry can gain a competitive edge and navigate the complexities of the market.

