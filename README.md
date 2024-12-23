# Data Analytics Internship Screening Assignment

## Overview
This project is part of the screening assignment for the **Data Analyst Internship** at **upliance.ai**. The task involves analyzing datasets related to **user behavior**, **cooking preferences**, and **order trends**. The datasets include **UserDetails**, **CookingSessions**, and **OrderDetails**. 
I have performed data cleaning, analysis, and generated key insights using **Python** (Pandas, NumPy) and visualizations with **Matplotlib** and **Seaborn**. The final analysis highlights the relationship between cooking sessions and user orders, identifies popular dishes, and explores demographic factors that influence user behavior.

## Project Objective
The objective of this assignment was to:
1. Clean and merge the **UserDetails**, **CookingSessions**, and **OrderDetails** datasets.
2. Analyze the relationship between cooking sessions and user orders.
3. Identify popular dishes and explore demographic factors influencing user behavior.
4. Create visualizations to highlight key insights.
5. Write a report summarizing findings and providing business recommendations.


## Key Tasks
1. **Data Cleaning**🧹: 
   - Handled missing values, duplicates, and inconsistencies across the three datasets.
   - Merged the datasets based on common fields (e.g., user ID, session ID).
   
2. **Data Transformation**🔄:
   - Aggregated data to analyze user trends.
   - Created new features to better understand user behavior.

3. **Exploratory Data Analysis (EDA)**🔍:
   - Analyzed relationships between **cooking sessions** and **orders**.
   - Identified popular dishes and uncovered patterns in user behavior based on **demographics**.

4. **Data Visualization**📊:
   - Visualized the most popular dishes, order trends, and user demographics using **Matplotlib** and **Seaborn**.
   - Created charts to showcase key insights.

5. **Reporting**📝:
   - Summarized findings in a report and provided actionable business recommendations.


## Questions Answered
1. **Identigy most popular dishes**🍝

2. **Understand the age distribution, location-wise concentration, and registration trends**📍

3. **Group users by Location to identify the most and least active locations.** 🌎


4. **Identify the most popular meals by counting the occurrences in Favorite Meal**🍽️

5. **Analyze the distribution of Total Orders to identify highly active users.** ⭐

6. **Calculate the average rating per session and identify sessions with the highest/lowest ratings** 🕒

7. **Analyze which times of the day (e.g., morning, afternoon, evening) are most popular for sessions** 😊

8. **Plot the distribution of Rating to see the general user satisfaction levels** 😊

9. **Identify Total Revenue and Average Revenue** 💰

## Tools and Technologies Used
- **Python**🐍
  - Pandas
  - NumPy
  - Matplotlib
  - Seaborn
- **Google Sheets** 📑 (for initial data review)

## Project Workflow
1. **Data Collection**📥: Data was collected in Google Sheets for initial exploration.
2. **Data Cleaning & Pre-processing**🧹: Used **Python** to clean and merge the datasets.
3. **Analysis**📊: Performed a detailed analysis using **Python** (Pandas, NumPy) to uncover insights.
4. **Visualization**📈: Created visualizations using **Matplotlib** and **Seaborn** to represent the key findings.
5. **Reporting**📝: Summarized the analysis and provided actionable business recommendations.



- ## ** Questions Answered with Code**  

## 1. **Most Popular Dishes**🍝

To identify the most popular dishes, we analyzed the **Dish Name** column in the dataset. The top 5 most popular dishes were determined by counting the occurrences of each dish in the data. Below is the Python code used to extract and display the top 5 dishes:

```python
popular_dishes = final_data['Dish Name_y'].value_counts().head(5)
print("Top 5 Popular Dishes:")
print(popular_dishes)
```
## Age Distribution, Location-wise Concentration, and Registration Trends

To understand the **age distribution**, **location-wise concentration**, and **registration trends**, the following analysis was performed:

### 2. **Age Distribution of Users**🎂

The age distribution of users was visualized using a histogram. This provides an overview of how users are distributed across different age groups.

Here’s the Python code used to plot the age distribution:

```python
user_details['Age'].hist(bins=10, color='skyblue', edgecolor='black')
plt.title('Age Distribution of Users')
plt.xlabel('Age')
plt.ylabel('Count')
plt.show()
```
## 3. **Group Users by Location to Identify the Most and Least Active Locations**🌍

To identify the most and least active locations based on the number of users, we grouped the users by their **Location** and counted the occurrences of each location.

### Code to Analyze Location Data:

```python
location_data = user_details['Location'].value_counts()
location_data.head()
```

## 4. **Identify the Most Popular Meals by Counting the Occurrences in Favorite Meal**🍽️

To identify the most popular meals, we analyzed the **Favorite Meal** column in the **user_details** dataset by counting how many times each meal was chosen as the favorite.

### Code to Identify Popular Meals:

```python
popular_meals = user_details['Favorite Meal'].value_counts()
print(popular_meals)
```
## 5. **Analyze the Distribution of Total Orders to Identify Highly Active Users**📊

To understand the distribution of **Total Orders** and identify highly active users, we visualized the distribution using a histogram. This analysis helps in identifying users with a high number of orders, which could indicate high engagement or loyalty.

### Code to Analyze the Distribution of Total Orders:

```python
# Analyze the distribution of Total Orders to identify highly active users
user_details['Total Orders'].hist(bins=10, color='orange', edgecolor='black')
plt.title('Distribution Of Total Orders')
plt.xlabel('Total Orders')
plt.ylabel('Count')
plt.show()
```
## 6. **Calculate the Average Rating per Session and Identify Sessions with the Highest/Lowest Ratings**⭐

To understand the quality of different sessions, we calculated the **average rating** per session and identified the sessions with the highest and lowest ratings.

### Code to Calculate Average Rating per Session:

```python
avg_rating = final_data.groupby('Session ID_x')['Session Rating'].mean()
print(avg_rating.sort_values(ascending=False).head(10))
```

## 7. **Analyze Which Times of the Day (e.g., Morning, Afternoon, Evening) Are Most Popular for Sessions**🕒

To understand which times of the day are most popular for sessions, we analyzed the **Time of Day** column and counted the occurrences of each time category (morning, afternoon, evening).

### Code to Analyze the Popular Times of the Day:

```python
time_of_day_counts = final_data['Time of Day'].value_counts()
print(time_of_day_counts)
```
## 8. **Plot the Distribution of Rating to See the General User Satisfaction Levels**😊

To analyze the general user satisfaction levels, we plotted the distribution of **Rating**. This helps in understanding how users are rating the sessions and provides insight into overall satisfaction.

### Code to Plot the Rating Distribution:

```python
# Plot the distribution of Rating to see the general user satisfaction levels
final_data['Rating'].hist(bins=5, color='green', edgecolor='black')
plt.title('Rating Distribution')
plt.xlabel('Rating')
plt.ylabel('Count')
plt.show()
```
## 9. **Identify Total Revenue and Average Revenue**💰

To understand the overall financial performance, we calculated the **Total Revenue** and **Average Revenue** based on the **Amount (USD)** column in the dataset. These metrics help in evaluating the revenue generation across all sessions.

### Code to Calculate Total Revenue and Average Revenue:

```python
total_revenue = final_data['Amount (USD)'].sum()
avg_revenue = final_data['Amount (USD)'].mean()
print(f"Total Revenue: ${total_revenue:.2f}, Average Revenue: ${avg_revenue:.2f}")
```
# Key Insights & Business Recommendations

## 1. Popular Dishes:🍝
**Spaghetti** is the most popular dish, with **9 occurrences**. This indicates a strong preference for pasta dishes, suggesting businesses could consider offering more varieties of spaghetti or promoting it in marketing campaigns to boost engagement.

## 2. Age Distribution:🎂
The age distribution shows values of **27.5** and **30**, which suggests that the users in this dataset are primarily in the late 20s to early 30s age group. This demographic is likely tech-savvy and may prefer modern, convenient food options.  
**Business Recommendation**: Target this age group with personalized offers, digital marketing, or easy-to-order meal options that fit their lifestyle.

## 3. Location-wise User Concentration:🌎
**New York**, **Los Angeles**, **Chicago**, **San Francisco**, **Seattle**, **Austin**, **Boston**, **Miami**, **Dallas**, and **Phoenix** all show **1 user** each. This indicates that the dataset includes users from various major U.S. cities, but there is no significant concentration in any one city.  
**Business Recommendation**: Identify areas for expansion or tailor marketing strategies for these locations. Since all locations have an equal distribution, focusing on broadening engagement in these regions could be worthwhile.

## 4. Most Popular Meals (Favorite Meal): 🍽️
**Dinner** is the most frequently chosen favorite meal, with **5 occurrences**. This suggests that users prefer having dinner-based meals.  
**Business Recommendation**: Restaurants and businesses might consider offering more dinner options or bundling them to attract customers who favor this meal type.

## 5. Active Users Based on Total Orders:📈
Users with **8** and **14 total orders** are identified as highly active. These users place more than **2 orders** on average, indicating they are engaged and loyal.  
**Business Recommendation**: Target these active users for **loyalty programs** or special offers. Identifying their behaviors and preferences can help tailor offerings to increase engagement further.

## 6. Session Ratings:⭐
**S015** received a perfect rating of **5.0**, indicating it was the top-rated session. This could suggest that the session content or user experience was exceptional.  
**Business Recommendation**: Analyzing the characteristics of sessions with high ratings can help businesses replicate successful strategies for other sessions.

## 7. Most Popular Times of Day for Sessions:🕒
**Night** is the most popular time for sessions, with **15 occurrences**. This indicates that users are more likely to engage with sessions during the evening or night hours.  
**Business Recommendation**: Schedule sessions during the **evening or night** to capitalize on this peak engagement time.

## 8. Rating Distribution (User Satisfaction):😊
The ratings are mostly **4.0** and **4.2**, suggesting that users are generally satisfied with the sessions and services provided, but there is room for improvement to achieve higher ratings.  
**Business Recommendation**: Focus on improving services where ratings are slightly lower to boost user satisfaction and increase ratings above **4.0**.

## 9. Revenue Insights:💰
The **Total Revenue** is **$349.50**, and the **Average Revenue** is **$10.92**. This indicates that while individual sessions may not be generating large amounts of revenue, the cumulative revenue from all sessions is significant.  
**Business Recommendation**: Explore strategies to increase the **average revenue per session**, such as offering **premium packages** or upselling additional services to increase the overall revenue.

---

## Business Recommendations Summary:
- **Focus on Popular Dishes**🍝: Promote dishes like **Spaghetti**, which are most popular, through targeted marketing or meal bundles.
- **Target Key Demographics**🎯: Tailor marketing campaigns to users in the **late 20s to early 30s** age group, offering convenient meal options and loyalty rewards.
- **Location-Based Marketing** 📍: Consider expanding or promoting services in the cities where users are located, especially those that are underrepresented.
- **Leverage Highly Active Users**📈: Reward loyal users who place multiple orders to increase retention and foster long-term customer relationships.
- **Replicate High-Performing Sessions**⭐: Analyze the **S015 session** to understand why it received a perfect rating and replicate its success in future sessions.
- **Optimize Evening/Night Sessions**🕒: Since **night sessions** are the most popular, businesses should focus on scheduling content during this time to capture the highest engagement.
- **Improve User Experience**😊: Focus on improving services where ratings are slightly lower to boost user satisfaction and increase ratings above **4.0**.
- **Increase Revenue** 💰: Explore ways to increase **average revenue** per user, like offering premium meal options or bundling popular items.


## Conclusion:
This analysis provides valuable insights into user behavior, meal preferences, and session performance. By understanding the most popular dishes, age demographics, and active users, businesses can make informed decisions on how to tailor their offerings and marketing strategies. The distribution of session ratings, user satisfaction, and revenue trends highlight areas for improvement as well as opportunities for growth.




