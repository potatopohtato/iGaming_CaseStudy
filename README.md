# Readme for Player Segmentation Case Study

## Overview
This case study focuses on player segmentation using a combination of datasets provided by Lognormal Analytics. The goal is to develop a comprehensive player segmentation strategy, validate the effectiveness of the segmentation model, and provide actionable insights for the business. The analysis includes data preprocessing, feature engineering, and the application of RFM (Recency, Frequency, Monetary) analysis combined with K-means clustering to segment players into distinct groups. The study also includes visualizations and recommendations for implementing the segmentation in practice.

## Methodology

### Data Preprocessing
1. **Data Cleaning**: 
   - Removed test cases from the `Player_Details` dataset.
   - Standardized column names across all datasets.
   - Handled null values in the `acquisition_channel` column by imputing normalized proportion percentages.
   - Expanded the granularity of the datetime column for better analysis.

2. **Feature Engineering**:
   - Chose key variables for RFM analysis: `Activitymonth` for Recency, `ActivePlayerDays` for Frequency, and `Net Gross Revenue` for Monetary value.
   - Merged `Player_Activity` and `BonusCost` datasets to calculate Net Revenue Generated.

### Segmentation Technique
- **RFM Analysis**: 
  - Calculated Recency, Frequency, and Monetary values for each player.
  - Normalized the RFM values using MinMaxScaler.
  - Applied K-means clustering with 4 clusters to segment players.

### Segmentation Results
Four distinct segments were identified:
1. **High-Value Loyal Players**: High frequency and monetary value, low recency.
2. **Casual Players**: Low frequency, mid to high monetary value, low recency.
3. **New/Low-Value Players**: Low frequency and monetary value, low recency.
4. **Potential Churners**: High frequency and monetary value, high recency.

### Validation
- Validated the clusters by computing the average RFM values per cluster and mapping them to intuitive segment labels.
- Visualized the correlations of RFM values and customer segments to ensure the effectiveness of the segmentation model.

### Implementation Recommendations
- **High-Value Loyal Players**: Offer loyalty rewards and exclusive offers to retain them.
- **Casual Players**: Encourage more frequent engagement through targeted promotions.
- **New/Low-Value Players**: Focus on onboarding and initial engagement strategies to increase their activity and value.
- **Potential Churners**: Implement re-engagement campaigns to bring them back into active play.

## Data Visualizations
- RFM Distributions
- Retention rate Distributions
- PLV Distributions

## Key Insights and Recommendations
- **Segmentation**: The RFM analysis combined with K-means clustering effectively segments players into meaningful groups.
- **Retention**: Trends in retention rates based on signup channels or platforms should be analyzed to identify potential causes and improve retention strategies.
- **Player Lifetime Value (PLV)**: Calculate PLV using available data and analyze the relationship between the first deposit amount and PLV. Recommend strategies to increase PLV for low-value players.

## Limitations and Suggestions
- **Limitations**: The datasets may have missing or incomplete data, which could affect the accuracy of the analysis.
- **Suggestions**: Additional data such as player demographics, game preferences, and more detailed transaction histories could enhance the analysis.

---
