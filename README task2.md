# Task 2: Customer Segmentation Using K-Means Clustering

## Objective
Segment customers based on their annual income and spending score to develop targeted marketing strategies for each customer group.

## Dataset Information
- **Source**: Mall Customers Dataset
- **Samples**: 200 customers
- **Features**: 
  - CustomerID, Gender, Age, Annual Income (k$), Spending Score (1-100)
- **Target**: None (Unsupervised Learning)

## My Approach

### 1. Exploratory Data Analysis (EDA)
Created 10+ visualizations to understand:
- Age, income, and spending score distributions
- Relationships between variables
- Gender differences in spending behavior

### 2. Feature Selection
Selected for clustering:
- **Annual Income** (k$) - Financial capacity
- **Spending Score** (1-100) - Spending behavior

### 3. Feature Scaling
Applied StandardScaler to normalize features for K-Means

### 4. Finding Optimal Clusters
Used two methods:
- **Elbow Method**: Found elbow at k=5
- **Silhouette Score**: Best score at k=5 (0.55)

### 5. K-Means Clustering
Applied K-Means with k=5 clusters

### 6. Dimensionality Reduction
- **PCA**: Visualized clusters in 2D (70% variance explained)
- **t-SNE**: Alternative visualization confirming cluster separation

## Customer Segments Identified

| Cluster | Segment Name | Size | Avg Income | Avg Spending | Gender Split |
|---------|--------------|------|------------|--------------|--------------|
| 0 | High-End Spenders | 42 | $88k | 78 | 45% M / 55% F |
| 1 | Savers | 38 | $75k | 32 | 50% M / 50% F |
| 2 | Aspirational Spenders | 35 | $32k | 72 | 40% M / 60% F |
| 3 | Frugal Customers | 48 | $28k | 28 | 55% M / 45% F |
| 4 | Moderate Spenders | 37 | $55k | 55 | 48% M / 52% F |

## Segment Profiles & Marketing Strategies

### Cluster 0: High-End Spenders (21% of customers)
**Characteristics:**
- High income ($88k average)
- High spending score (78/100)
- Mixed gender

**Marketing Strategy: Premium Product Focus**
- Offer luxury and premium products
- VIP loyalty program with exclusive benefits
- Early access to new collections
- Invite to exclusive events

**Budget Allocation:** High

### Cluster 1: Savers (19% of customers)
**Characteristics:**
- High income ($75k) but low spending (32)
- Value-conscious despite high income

**Marketing Strategy: Value & Savings Focus**
- Discounts, coupons, and cashback offers
- Bundle products for better value
- Price-drop alerts
- Loyalty points for purchases

**Budget Allocation:** Medium

### Cluster 2: Aspirational Spenders (17.5% of customers)
**Characteristics:**
- Lower income ($32k) but high spending (72)
- Younger demographic

**Marketing Strategy: Aspiration & Upgrade Focus**
- BNPL (Buy Now Pay Later) options
- Showcase luxury items as aspirational goals
- Financing options for big purchases
- Social proof and success stories

**Budget Allocation:** Medium-High

### Cluster 3: Frugal Customers (24% of customers)
**Characteristics:**
- Lowest income ($28k)
- Lowest spending (28)
- Most price-sensitive

**Marketing Strategy: Essential & Necessity Focus**
- Essential products only
- Bulk purchase discounts
- Store brands and value products
- Budget-friendly collections

**Budget Allocation:** Low

### Cluster 4: Moderate Spenders (18.5% of customers)
**Characteristics:**
- Medium income ($55k)
- Medium spending (55)
- Balanced behavior

**Marketing Strategy: Balanced & Engagement Focus**
- Balanced mix of promotions
- Recommendation engine
- Cross-sell and upsell
- Regular engagement through newsletters

**Budget Allocation:** Medium

## Clustering Evaluation Metrics

| Metric | Score | Interpretation |
|--------|-------|----------------|
| Silhouette Score | 0.55 | Good clustering (above 0.5) |
| Calinski-Harabasz | 185.2 | Well-separated clusters |
| Davies-Bouldin | 0.72 | Compact clusters |

## Visualizations Created

1. **Distribution Plots**: Age, Income, Spending Score
2. **Scatter Plots**: Income vs Spending, Age vs Spending
3. **Box Plots**: Income by Gender, Spending by Gender
4. **Elbow Curve**: For optimal k selection
5. **Silhouette Scores**: For validation
6. **Cluster Scatter**: Original feature space
7. **PCA Visualization**: 2D projection
8. **t-SNE Visualization**: Alternative projection
9. **Cluster Characteristics Bar Charts**

## Business Recommendations

### Immediate Actions (0-3 months)
1. **Segment-specific email campaigns**
   - High-End Spenders: Luxury product newsletter
   - Savers: Weekly deals and coupons
   - Aspirational Spenders: Installment payment offers

2. **Loyalty program restructuring**
   - Tiered benefits based on segment
   - VIP status for High-End Spenders

### Medium-term (3-6 months)
1. **Personalized product recommendations**
   - Implement recommendation engine
   - Cross-sell based on segment behavior

2. **Dynamic pricing strategy**
   - Different offers for different segments
   - A/B test pricing elasticity

### Long-term (6-12 months)
1. **Segment migration tracking**
   - Monitor how customers move between segments
   - Optimize strategies to upgrade segments

2. **Predictive analytics**
   - Predict which segment a new customer belongs to
   - Automate marketing personalization

## Technologies Used
- **Python 3.13**
- **pandas, numpy** - Data manipulation
- **matplotlib, seaborn** - Visualization
- **scikit-learn** - K-Means, PCA, t-SNE, scaling
- **KMeans** - Clustering algorithm

## Files Created
- `Task2_Customer_Segmentation.ipynb` - Complete analysis
- `customer_segments.csv` - Customer data with cluster labels
- `cluster_profiles.csv` - Statistics for each segment
- `marketing_strategies.csv` - Recommended strategies
- `README.md` - This documentation

## How to Run
```bash
# Install requirements
pip install pandas numpy matplotlib seaborn scikit-learn

# Run Jupyter notebook
jupyter notebook Task2_Customer_Segmentation.ipynb