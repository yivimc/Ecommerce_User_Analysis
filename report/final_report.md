# E-commerce User Behavior Analysis Report

## 1. Project Background

With the rapid development of e-commerce platforms, user behavior data has become one of the most valuable assets for business decision-making. By analyzing browsing, favorite, cart, and purchase behaviors, enterprises can better understand customer preferences, optimize conversion paths, and improve customer lifetime value.

This project utilizes the Alibaba Tianchi UserBehavior Dataset to conduct a comprehensive analysis of user behaviors. The analysis focuses on four key aspects:

* User behavior distribution
* User activity patterns
* Conversion funnel analysis
* RF-based customer segmentation

The goal is to identify user behavior characteristics and provide data-driven recommendations for platform operations and precision marketing.

---

## 2. Dataset Description

### Data Source

Alibaba Tianchi UserBehavior Dataset

### Data Fields

| Field         | Description                 |
| ------------- | --------------------------- |
| user_id       | User Identifier             |
| item_id       | Product Identifier          |
| category_id   | Product Category Identifier |
| behavior_type | User Behavior Type          |
| timestamp     | Unix Timestamp              |

### Behavior Types

| Behavior Type | Meaning     |
| ------------- | ----------- |
| pv            | Page View   |
| fav           | Favorite    |
| cart          | Add to Cart |
| buy           | Purchase    |

### Data Scale

After random sampling and preprocessing:

* Total Records: 2,003,016
* Purchase Users: 38,697
* User Behaviors: PV, Favorite, Cart, Purchase

---

## 3. Data Preprocessing

The following preprocessing procedures were conducted:

### 3.1 Data Sampling

To improve computational efficiency, 2% random sampling was performed on the original dataset.

### 3.2 Timestamp Conversion

Unix timestamps were converted into datetime format.

Additional features were generated:

* Date
* Hour
* Weekday

### 3.3 Data Quality Inspection

The dataset was examined for:

* Missing values
* Duplicate records
* Data type consistency

No significant data quality issues were identified.

---

## 4. User Behavior Analysis

### 4.1 Behavior Distribution

The distribution of user behaviors is shown below:

| Behavior | Percentage |
| -------- | ---------- |
| PV       | 89.57%     |
| Cart     | 5.51%      |
| Favorite | 2.90%      |
| Buy      | 2.02%      |

### Findings

The majority of user interactions are browsing activities.

Purchase behaviors account for only a small proportion of total actions, indicating a substantial gap between user interest and actual transaction completion.

This suggests that conversion optimization remains an important opportunity for platform growth.

---

### 4.2 User Activity Analysis

User activity was analyzed by hour and weekday.

### Findings

User activity exhibits clear temporal patterns.

The highest activity levels occur during evening hours, particularly between 18:00 and 23:00.

This behavior suggests that users tend to browse and shop after work or study hours.

### Business Implication

Marketing campaigns, promotional notifications, and advertising activities should be concentrated during peak activity periods to maximize engagement.

---

### 4.3 Popular Products and Categories

Top-performing products and categories were identified through frequency analysis.

### Findings

Several products and categories receive significantly more user interactions than others, indicating concentrated demand within certain market segments.

### Business Implication

Popular products should be prioritized in recommendation systems and promotional campaigns.

High-performing categories may also provide valuable insights for inventory planning and product strategy.

---

## 5. Conversion Funnel Analysis

A simplified conversion funnel was constructed using user behavior data.

### Funnel Statistics

| Stage          |   Users |
| -------------- | ------: |
| Page View (PV) | 676,221 |
| Favorite (FAV) |  48,190 |
| Cart           |  96,281 |
| Purchase (BUY) |  38,697 |

### Findings

A significant number of users browse products but do not proceed to purchase.

The shopping cart stage demonstrates the strongest purchase intent among intermediate actions.

Approximately 40% of cart users eventually complete a purchase.

### Business Implication

The shopping cart represents a critical conversion point.

Improving cart reminder mechanisms, promotional incentives, and checkout experience may significantly increase overall conversion rates.

---

## 6. RF Customer Segmentation Analysis

### 6.1 Methodology

Due to the absence of transaction amount information, a simplified RF model was adopted.

#### Recency (R)

Number of days since the user's last purchase.

#### Frequency (F)

Number of completed purchases.

Users were scored according to predefined business rules and categorized into different customer groups.

---

### 6.2 Segmentation Results

| Segment        |  Users |
| -------------- | -----: |
| Low Value User | 19,530 |
| Active User    | 17,525 |
| Core User      |  1,060 |
| At Risk User   |    582 |

### Findings

The user structure exhibits a clear pyramid distribution.

More than half of users belong to the low-value segment, while core users represent only a small proportion of the customer base.

Although the core user group is relatively small, it demonstrates higher purchasing frequency and stronger loyalty.

The at-risk segment consists of users who have historically shown purchasing activity but have recently become inactive.

---

## 7. Key Business Insights

### Insight 1

User behavior is dominated by browsing activities.

A large volume of traffic exists at the top of the funnel, but only a small proportion converts into purchases.

### Insight 2

User activity is concentrated during evening hours.

This period should be prioritized for promotional campaigns and customer engagement activities.

### Insight 3

The shopping cart serves as the most important transition stage between user interest and purchase.

Cart abandonment reduction may generate substantial revenue improvements.

### Insight 4

Active users represent the largest growth opportunity.

Targeted marketing strategies may help convert active users into core users.

### Insight 5

Core users contribute disproportionate business value despite their small population size.

Maintaining their loyalty should be a strategic priority.

---

## 8. Business Recommendations

### Recommendation 1: Strengthen Customer Retention

Develop membership programs and loyalty incentives for core users.

Potential initiatives include:

* VIP programs
* Exclusive discounts
* Reward points systems
* Early access to new products

---

### Recommendation 2: Improve Conversion Performance

Enhance product detail pages and checkout experiences.

Potential measures include:

* Personalized recommendations
* Product bundling
* Limited-time promotions

---

### Recommendation 3: Re-engage At-Risk Users

Implement targeted retention campaigns.

Potential measures include:

* Coupon distribution
* Price-drop notifications
* Personalized reminders

---

### Recommendation 4: Increase User Engagement

Encourage low-value users to interact more frequently with the platform through:

* New-user incentives
* Gamified activities
* Product discovery campaigns

---

## 9. Project Conclusion

This project analyzed over two million e-commerce user behavior records and explored user activity patterns, conversion performance, and customer value segmentation.

The analysis revealed that:

* Browsing behaviors dominate platform interactions.
* User activity peaks during evening hours.
* The shopping cart is a critical conversion stage.
* Customer value distribution follows a typical pyramid structure.

Based on these findings, several operational recommendations were proposed, including customer retention programs, conversion optimization strategies, and targeted user segmentation initiatives.

The methodology and insights generated in this project can serve as a practical reference for data-driven decision-making in e-commerce operations.
