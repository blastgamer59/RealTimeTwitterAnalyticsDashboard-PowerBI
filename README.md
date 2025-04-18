# RealTimeTwitterAnalyticsDashboard-PowerBI

## Project Overview
This project provides comprehensive analytics on Twitter engagement metrics through a series of interactive visualizations created in Power BI. The dashboards offer insights into tweet performance, engagement patterns, and user interaction trends with specific filtering capabilities for detailed analysis.

## Technical Stack
- **Power BI Desktop**: Core visualization and dashboard creation tool
- **DAX (Data Analysis Expressions)**: For creating calculated measures and columns
- **Power Query (M)**: For data transformation, cleaning, and preparation
- **Custom Filters**: Time-based, engagement-based, and content-based filtering

## Completed Visualizations

### 1. High Engagement Rate Tweet Analysis
- **Chart Type**: Bar chart with filters
- **Metrics**: Engagement rates (top 10%)
- **Filters**:
  - Likes > 50
  - Weekday posts only
  - Time filter: 1 PM to 4 PM
  - Tweet word count < 30
- **Implementation**: Created calculated columns for word count and extracted day of week for filtering

### 2. Total Clicks Distribution for High-Impression Tweets
- **Chart Type**: Pie chart with drill-down capability
- **Metrics**: URL clicks, profile clicks, hashtag clicks
- **Filters**: Tweets with > 500 impressions
- **Drill-down**: From total clicks to specific click types per tweet

### 3. Time-Based Engagement Analysis (Jan-Jun 2020)
- **Chart Type**: Line chart with dual metrics
- **Metrics**: Average engagement rate and total impressions
- **Filters**:
  - Date range: '01-01-2020' to '30-06-2020'
  - Impressions > 100
  - Likes = 0
  - Time filter: 3 PM to 5 PM IST only

### 4. Interaction Types by Tweet Category
- **Chart Type**: Clustered bar chart
- **Metrics**: Sum of URL clicks, profile clicks, hashtag clicks by category
- **Categories**: Tweets with media, links, hashtags
- **Filters**:
  - Time: 3 PM to 6 PM
  - Tweet date: Even-numbered dates only
  - Word count < 40
  - At least one interaction type
- **Implementation**: Created category flags based on tweet content analysis

### 5. Top 10 Tweets by Engagement
- **Chart Type**: Bar chart with user profile information
- **Metrics**: Sum of retweets and likes
- **Filters**:
  - Weekday posts only
  - Time: 3 PM to 6 PM
  - Tweet impressions: Even numbers only
  - Tweet date: Odd-numbered dates only
  - Word count < 30

### 6. Media Engagement vs. Views Analysis
- **Chart Type**: Scatter plot with conditional formatting
- **Metrics**: Media engagements (y-axis), media views (x-axis)
- **Filters**:
  - Replies > 10
  - Time: 12 PM to 6 PM
  - Tweet date: Odd-numbered dates only
  - Word count < 50
- **Highlight**: Tweets with engagement rate > 5%

### 7. Media Interactions by Day of Week
- **Chart Type**: Dual-axis chart
- **Metrics**: Media views (primary axis), media engagements (secondary axis)
- **Period**: Last quarter
- **Filters**:
  - Time: 3 PM to 6 PM
  - Tweet impressions: Even numbers only
  - Tweet date: Odd-numbered dates only
  - Word count < 30
- **Highlight**: Days with significant interaction spikes

### 8. App Opens Impact on Engagement
- **Chart Type**: Comparison chart
- **Metrics**: Engagement rate for tweets with vs. without app opens
- **Filters**:
  - Posted between 9 AM and 5 PM on weekdays
  - Time filter: 12 PM to 6 PM
  - Tweet impressions: Even numbers only
  - Tweet date: Odd-numbered dates only
  - Word count < 40

### 9. Monthly Engagement Rate Trends
- **Chart Type**: Line chart with multiple series
- **Metrics**: Average engagement rate by month
- **Series**: Tweets with media vs. tweets without media
- **Filters**:
  - Time: 3 PM to 6 PM
  - Tweet engagement: Even-numbered values only
  - Tweet date: Odd-numbered dates only

### 10. Summer 2020 High Media Engagement Analysis
- **Chart Type**: Comparative visualization
- **Metrics**: Replies, retweets, and likes
- **Filters**:
  - Media engagements > median value
  - Date range: June to August 2020
  - Time: 3 PM to 6 PM
  - Tweet date: Odd-numbered dates only
  - Media views: Even numbers only
  - Word count < 50

## Implementation Details

### Data Preparation
- Created date and time tables for proper time intelligence
- Developed calculated columns for day of week, word count, etc.
- Created engagement rate calculations and threshold measures

### Custom Filter Implementation
- Implemented dynamic time-based filtering 
- Created parameters for user-adjustable thresholds
- Designed slicers for interactive filtering

### Performance Optimization
- Implemented query optimization techniques
- Used appropriate aggregation methods
- Created calculated tables where necessary for improved performance

### Data Cleaning
- **Missing Value Handling**: Identified and addressed null values in engagement metrics
-  Replaced missing impression values with averages from the same time of day
-  Removed tweets with no identifiable timestamp or user information
-  Created flags for tweets with incomplete metric sets
- **Data Type Standardization**: Converted all date/time fields to proper format
-  Fixed inconsistent date formats from different data sources
-  Standardized timestamp data to include timezone information
-  Ensured numeric fields were properly recognized as numbers not text


### Data Transformation
- **Tweet Content Analysis**:
  - Created word count column by parsing tweet text
  - Extracted hashtags and mentions into separate fields
  - Identified links and media attachments
  - Categorized tweets based on content type (promotional, informational, etc.)

## Conclusion
This project delivers comprehensive Twitter analytics capabilities with precise filtering mechanisms and insightful visualizations. The implemented dashboards enable data-driven decision making for social media strategy optimization.
