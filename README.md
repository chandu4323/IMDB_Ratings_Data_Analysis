# Project: Detailed Analysis of IMDb Ratings and Worldwide Gross Revenue - Jupyter Notebook - Python, SQL, Pandas

**Problem Description:**
Understanding the intricate relationship between IMDb ratings and worldwide gross revenue is paramount for stakeholders in the film industry. The significance of this problem lies in its potential to inform decision-making processes related to filmmaking, investment, and strategic planning. For filmmakers, it provides insights into how critical acclaim translates into financial success, guiding choices in genres, marketing, and resource allocation.

**Approach and Methods:**

**CSV Parsing and Denormalized Database Creation:**
1.  A robust CSV parsing function was developed to extract relevant movie information from the IMDbMovies-Clean.csv file.
2.  An SQLite database, denormalized.db, was created, along with a "Denormalized" table to store raw movie data.

**Data Normalization:**
1.  To structure and organize data effectively, a normalization process was implemented.
2.  This involved connecting to both denormalized.db and a new normalized database, normalized.db.
3.  Defined normalized tables (Movie, Director, Writers, and Financials) and mapped data from the denormalized table using foreign keys.

**Data Visualization:**
1.  Jupyter widgets, pandas, plotly.express, and ipywidgets were leveraged to enhance user interaction and provide a visual representation of IMDb ratings.
2.  An interactive bar plot was created, allowing users to explore IMDb ratings based on selected genre and release year.

**Data Analysis:**
1.  A Dash web application was developed to offer users a dynamic and interactive environment for exploring the movie dataset.
2.  Correlation analyses, scatter plots, and statistical tests were conducted to delve into the relationships between IMDb ratings and financial metrics.

**Correlation Analysis:**
1.  A weak positive correlation (0.15) between IMDb Ratings and Gross Worldwide Revenue was observed.
2.  The scatter plot visually highlighted the variability in revenue for movies with similar ratings, emphasizing the influence of unexplored factors.
3.  A weak positive correlation (0.15) between IMDb Ratings and Gross Worldwide Revenue was observed.
4.  The scatter plot visually highlighted the variability in revenue for movies with similar ratings, emphasizing the influence of unexplored factors.

**Linear Regression:**

1.  Ordinary Least Squares (OLS) regression analysis was employed to quantify the relationship between IMDb ratings and gross worldwide revenue.
2.  The statistical significance and explanatory power of IMDb ratings in predicting revenue were assessed.
3.  The OLS regression analysis demonstrated that IMDb Rating is statistically significant in predicting Gross Worldwide Revenue.
4.  However, the model's limited explanatory power (R^2: 2.1%) suggested that IMDb Rating alone cannot fully account for the variability in revenue.
5.  A positive association between IMDb ratings, budgets, and gross worldwide revenue was established, but the R-squared value remained low (2.3%) in multiple linear regression.

**Multiple Linear Regression Analysis:**

1.  Multiple linear regression analyses were performed, considering different independent variables such as release year, runtime, number of ratings, budget, gross US/Canada revenue, and gross worldwide revenue.
2.  The multiple linear regression model explained 30.3% of IMDb rating variance.
3.  ReleaseYear, Runtime, and NumberOfRatings emerged as influential factors.
4.  A potential trade-off between global box office success and IMDb ratings was indicated by the negative coefficient for GrossWorldWide.
