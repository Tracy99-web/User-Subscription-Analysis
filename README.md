# **Project Description**

This project analyzes Netflix subscription data to understand user behavior, retention rates, and revenue trends. By examining different subscription types, demographics, and device usage, the analysis aims to offer actionable insights to improve product strategies and customer engagement.

# **Technologies Used**

- **Tools**: Power BI, Tableau, Python, Pandas
- **Data Analysis Libraries**: `pandas`, `matplotlib`, `seaborn`
- **Visualizations**: Bar Charts, Line Graphs, Pie Charts

# Skills Demonstrated

- Statistical Analysis
- Data Visualization
- Churn Analysis
- Exploratory Data Analysis

# **Methodology**

**Step 1: Data Loading**

- **Code**: Used `pd.read_csv()` to load the dataset.
- **Explanation**: Loading the data is essential to bring it into the environment for manipulation and exploration.

**Step 2: Data Cleaning**

- **Code**: Checked for missing values with `.isnull().sum()`, handled missing entries with `.fillna()` or `.dropna()`, and ensured date formats were consistent.
- **Explanation**: Data cleaning ensures accuracy and reliability, preparing the dataset for meaningful analysis.

**Step 3: Exploratory Data Analysis (EDA)**

- **Data Structure**: Used `.info()` and `.describe()` to understand data types, non-null counts, and summary statistics for numerical columns.
- **Initial Insights**: Analyzed basic stats for monthly revenue, age, and plan duration.
- **Frequency Distribution**: Analyzed categorical columns like `Subscription Type`, `Country`, `Gender`, and `Device` to understand the distribution of users.
    - **Subscription Type Frequency**: Counted users in each type (Premium, Standard, Basic).
    - **Country Distribution**: Counted users by country to see regional distribution.
    - **Gender Distribution**: Checked the balance between male and female users.
    - **Device Usage**: Analyzed which devices (e.g., mobile, desktop, smart TV) were most used for streaming.
- **Explanation**: EDA helps understand the data structure, distribution, and any obvious patterns, guiding further analysis.

**Step 4: Revenue Analysis**

- **Average Revenue by Subscription Type**: Used `.groupby("Subscription Type")["Monthly Revenue"].mean()` to calculate average revenue.
- **Revenue by Device and Country**: Aggregated revenue data to compare average revenue by device type and country.
- **Explanation**: This step helps Netflix identify which plans and user segments contribute most to revenue, essential for optimizing pricing strategies.

**Step 5: Retention and Churn Analysis**

- **Churn Definition**: Defined churned users as those whose `Last Payment Date` exceeded 30 days from the reference date (15th July 2023).
- **Churn Rate by Subscription Type**: Calculated the proportion of churned users within each subscription type.
- **Retention Rate by Demographic**: Examined retention rates by age group, gender, and country.
- **Explanation**: Retention analysis helps identify which user segments may require more targeted engagement strategies to reduce churn.

**Step 6: Subscription Duration Analysis**

- **Months Subscribed Calculation**: Created a `Months Subscribed` column by calculating the time difference between `Join Date` and the reference date.
- **Average Subscription Duration by Subscription Type**: Calculated average months subscribed for each subscription type.
- **Explanation**: This analysis provides insight into user loyalty and satisfaction by plan, informing decisions on plan features and retention efforts.

**Step 7: Frequency Distribution Analysis**

- **Subscription Type Frequency Distribution**: Counted the number of users by each subscription type.
- **Country-Based Distribution**: Analyzed how many users are in each country and their subscription types.
- **Device-Based Frequency Distribution**: Counted device usage frequency to see which devices are most popular.
- **Age Distribution**: Used histograms to visualize the distribution of user ages.
- **Explanation**: Frequency distributions reveal demographic and usage patterns, which are valuable for tailoring marketing and content strategies.

**Step 8: Visualization of Key Metrics**

- **Revenue by Subscription Type**: Created bar charts to display average revenue by subscription type.
- **Retention Rates by Country**: Visualized retention rates across countries to identify regional retention patterns.
- **Subscription Duration by Age Group**: Used line graphs to show average subscription duration by age group.
- **Device Usage**: Displayed device distribution with a bar chart to see device preferences.
- **Explanation**: Visualization makes complex metrics accessible and understandable, providing strategic insights for the Netflix team.

# Key Insights

### Subscription Trends

**Popular Subscription Plans:** The majority of users subscribed to Basic/Standard/Premium plans, with the Basic plan being the most popular. This suggests that most users do not prioritize specific feature such as HD content or simultaneous streams.

**Subscription Duration:** Users tend to retain their subscriptions for an average of 10 months which could indicate either a strong product engagement and value perception or that despite initial engagement, they ultimately find that Netflix does not sufficiently adapt to their changing interests.

### Demographic Analysis

**Age and Gender Distribution:** The largest subscriber segment falls within the 40-43 age group, with females slightly outnumbering males. This demographic profile provides insights into the target audience for tailored content and marketing campaigns.

**Regional Popularity:** Subscriptions are notably higher in the United States and Spain, indicating that Netflix’s content library resonates particularly well in this area. This could inform region-specific content development and advertising efforts.

### Churn Analysis

**Churn Rate:** The overall churn rate is approximately 0.04%, with a higher rate among users on the Basic plan. This insight suggests potential areas for improvement and offers for users on the Basic plan.

### Revenue Insights

**Revenue Distribution by Plan:** The Basic plan contributes the highest revenue share, though it has the cheapest subscription rate . This demonstrates that lower-tier plans, though niche, are crucial for revenue maximization.

### **Recommendations**

**Targeted Upsell Campaigns:** Develop targeted marketing campaigns aimed at Basic plan users who exhibit viewing habits indicative of a potential interest in higher-tier plans. Highlight features that align with their preferences to encourage upgrades.

**Incentivize Upgrades:** Consider offering limited-time promotions or discounts for Basic users who upgrade to Standard or Premium plans to make the transition more appealing.
Feedback Loop: Implement feedback mechanisms to gather insights from Basic plan users about their needs and preferences, which can inform future content offerings and feature enhancements in higher-tier plans.
