# Shopify App Analysis with Power BI

## Overview

This project explores the landscape of apps on the Shopify platform by analyzing public data scraped from Shopify websites. The goal is to identify key factors contributing to the success of a Shopify app using Power BI as the primary analytical tool. This project is structured into three main parts, each corresponding to a different aspect of the app ecosystem: App Landscape, Reviews, and App Reviews. 

### Dataset

The dataset, `shopify.xlsx`, contains data from the Shopify App Store across seven tables:

- **apps**: Details of apps available on the Shopify apps marketplace.
- **apps_categories**: Join table to connect apps with categories.
- **categories**: Categories of the apps. Each app belongs to multiple categories.
- **reviews**: User opinions about apps, including rating, comment, and developer response if available.

## Methodology

### Part 1: App Landscape

The objective is to understand the types of apps available. Key visualizations and their methods are as follows:

- **KPI Card**: Displays the unique number of apps. 
- **Line Chart**: Shows the sum of the review count over time, using the `lastmod` date.
- **Scatterplot**: Plots `reviews_count` vs. average rating to analyze the relationship between popularity and quality.

### Part 2: Reviews

Focuses on analyzing the reviews data to gauge user sentiment and developer engagement.

- **Helpful Reviews Calculation**: A new column, `helpful_reviews`, is created using DAX to weigh reviews by their helpfulness.
- **Developer Response Analysis**: A column, `developer_answered`, indicates whether a developer responded to a review. A scatterplot compares average ratings to developer responsiveness.

### Part 3: App Reviews

Links app data with reviews to evaluate app performance and developer activity.

- **Relationship Creation**: A new relationship between the Reviews and Apps tables allows for more detailed analysis.
- **Developer Performance Chart**: A bar chart showing the sum of ratings per developer to understand who is performing well overall.
- **Helpful Review Analysis**: Adjusts for the quantity of reviews by comparing the average `helpful_review` score per developer.
- **Responsiveness Chart**: Identifies the most responsive developers based on the `developer_answered` metric, focusing on those with a substantial number of reviews.

## Screenshots

Since PowerBI files are massive, each part of the project includes screenshots of the Power BI visualizations to illustrate the findings and support the analysis.

## Conclusion

This project provides a comprehensive overview of the Shopify app landscape through data-driven analysis. By understanding the factors that contribute to app success, developers and business strategists can make informed decisions to improve app performance and user satisfaction.
