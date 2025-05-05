## About

This project aims to support a restaurant consolidator in enhancing their B2C portal through intelligent, data-driven insights. Using a dataset originally sourced from Zomato via Kaggle, the analysis explores key factors such as cuisine variety, pricing, delivery availability, customer ratings, and regional trends. While it does not directly identify specific “star” restaurants, the project uncovers meaningful patterns and metrics that can inform better decision-making. Python was used for data cleaning and exploratory analysis, and Tableau was leveraged to build an interactive dashboard that empowers users to explore the restaurant landscape in a dynamic and insightful way.

## Project Overview
The aim of this project is to help stakeholders understand what makes a restaurant successful across various geographies. Using Python for data wrangling and exploratory analysis, and Tableau for building an interactive dashboard, the project offers clear insights into factors like cuisine diversity, service offerings, cost, and user ratings—without relying on advanced prediction or recommendation algorithms. This approach empowers users to derive their own conclusions using the data.

## Tools and Technologies Used
- **Pandas, NumPy** – for data manipulation and preprocessing
- **Matplotlib, Seaborn** – for data visualization during EDA
- **Jupyter Notebook** – for code execution and documenting the analysis workflow
- **Tableau** – for building an interactive dashboard with filters and visual insights
- **Draw.io, Figma, Photopea** – for planning dashboard layout and design aesthetics

## Datasets Used
- **data.xlsx** – Main dataset containing restaurant-level attributes such as name, location, cuisine types, pricing, ratings, votes, and service options
- **Country-Code.xlsx** – Supplementary file mapping country codes to their respective country names
- **exploded_cuisine_data.csv** – A preprocessed version of the main dataset where multi-cuisine entries were separated to support more granular visual analysis in Tableau

## Key Steps and Methodology
**1. Data Inspection and Cleaning **
        - Loaded and explored two datasets: one with restaurant-level information and another mapping country codes to country names
        - Identified and handled missing values, nulls, and inconsistent entries
        - Removed duplicate records to ensure dataset accuracy and reliability
        - Performed structural adjustments such as renaming columns for clarity and correcting data types

**2. Data Integration and Transformation**
        - Merged the datasets to enrich restaurant data with country names
        - Processed the 'Cuisines' column by splitting multi-cuisine values and generating a separate dataset for cuisine-level analysis
        - Standardized categorical variables and normalized inconsistent values (e.g., country names, currency formats)
        
**3. Exploratory Data Analysis (EDA)**
        - Analyzed geographic distribution of restaurants to identify country-wise and city-wise trends
        - Explored the presence and popularity of restaurant franchises across different regions
        - Investigated booking and delivery service availability, vote distribution, average costs, and their relationship with ratings
        - Identified top cuisines, frequency of cuisine offerings, and customer preference patterns
        - Evaluated how cost, delivery options, and variety of cuisines impact customer engagement and ratings

**4. Data Export and Preparation for Visualization**
        - Cleaned and aggregated data was exported to .csv format for use in Tableau
        - Separate datasets were structured to support different types of visual elements such as bubble charts, treemaps, and scatterplots
        
**5. Dashboard Planning and Design**
        - Created dashboard layout wireframes using Draw.io and Figma for structured and user-friendly design
        - Used Photopea to customize icons and visuals for consistency in visual storytelling
        - Implemented the dashboard in Tableau with fixed layout, floating containers, and region-specific filters

**6. Interactive Visualization and Insights**
        - Built dynamic visual components such as:
            - Executive KPIs for total restaurants, delivery/table booking percentages, and cost averages
            - Bubble charts for cuisine popularity
            - Bar charts ranking franchises by vote counts
            - Scatterplots analyzing the relationship between cost and rating
            - Treemaps highlighting top-voted restaurants by region
        - Added interactive filters for country and city, enabling targeted insights

## Key Insights
- **India-Centric Distribution**: The dataset is heavily skewed toward India, with over 90% of the entries belonging to Indian cities—particularly New Delhi, Bangalore, and Mumbai. This imbalance was evident both in the raw data and visual distribution maps. Countries like Canada, Brazil, and the UAE had very limited representation, making it difficult to generalize findings or build global recommendations without introducing geographic bias.
- **Skewness in Attributes**: Several numeric variables, including 'Votes' and 'Average Cost for Two', exhibited high positive skewness, with long tails concentrated around lower values. This uneven distribution impacts statistical interpretation and visual scaling. Future analysis may benefit from applying log transformation or normalization techniques to mitigate skewed effects and improve model performance or visual comparability.
- **Service Availability Gaps**: Only around 12.1% of restaurants in the dataset offer table booking, while about 25.7% provide online delivery. This disparity highlights varying levels of service accessibility and digital adoption across regions. These metrics were clearly reflected in both the Python-based EDA and executive-level KPIs on the Tableau dashboard.
- **Culinary Trends and Customer Engagement**: North Indian, Chinese, and Fast Food emerged as the top three cuisines served across most cities. Restaurants offering a greater variety of cuisines and delivery services consistently received higher ratings and more votes, suggesting a correlation between customer engagement and service diversity. This was supported by scatterplots comparing ratings against cost, cuisine count, and delivery flags.
- **Brand-Level Insights**: Prominent franchises such as Barbeque Nation, Big Chill, and Truffles stood out for their consistent popularity, high vote counts, and geographic spread. These patterns were validated through grouped analysis in Python and visualized via Tableau bar charts and treemaps.
- **Critical Perspective**: While the dataset enables meaningful EDA and dashboarding, its heavy concentration on one country limits its global applicability. For example, Brazil and Canada have fewer than 10 restaurants represented, making it difficult to derive actionable insights or build fair recommendation systems for those markets. Any recommendation framework based solely on this data would likely overfit to Indian consumer behavior.
- **Future Considerations**: Addressing skewness through log transformation, improving country-wise data representation, and applying machine learning models such as collaborative filtering or content-based recommendations could significantly enhance future analysis. However, such extensions require more balanced datasets and deeper user interaction metadata to be effective.

## Dashboard Access
[Click here to view the interactive dashboard on Tableau Public](https://public.tableau.com/app/profile/aastha.rai1316/viz/RestaurantInsights_17461496768120/ExecutiveDashboard)
