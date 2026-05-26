## 🎧 SPOTIFY USER SEGMENTATION

## 📌 Project Overview

This project focuses on performing User Segmentation on Spotify user behavior data using Unsupervised Machine Learning techniques.

The main objective is to identify different categories of Spotify users based on their listening behavior, engagement patterns, and interaction metrics. The project applies multiple clustering techniques and preprocessing methods to determine the best segmentation strategy.

The workflow includes:

- Data preprocessing
- Feature engineering and selection
- Running multiple clustering experiments
- Selecting the best clustering iteration
- User segmentation
- Cluster profiling
- Persona generation
- Visualization and insights extraction

---

# 🚀 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Apache Spark (Databricks Environment)

---

# 📂 Dataset Information

The project uses two datasets:

## 1. spotify_user_behavior
Contains behavioral listening metrics of users.

### Features Used:
- daily_listening_minutes
- sessions_per_day
- days_active_last_30
- avg_session_minutes
- skip_rate
- liked_songs_pct
- ads_skipped_pct

---

## 2. spotify_user_demo
Contains demographic details of users.

### Demographic Features:
- age
- country
- city_tier
- device_type
- subscription_tenure_months

---

# ⚙️ Clustering Algorithms Used

## 1. K-Means Clustering
Used for partition-based clustering.

## 2. Gaussian Mixture Models (GMM)
Used for probabilistic clustering with different covariance structures:
- Full
- Tied
- Diagonal
- Spherical

---

# 🔄 Preprocessing Techniques Used

Different preprocessing and transformation techniques were applied before clustering:

- No Scaling (Raw)
- StandardScaler
- RobustScaler
- MinMaxScaler
- PowerTransformer (Yeo-Johnson)
- PowerTransformer (Box-Cox)
- QuantileTransformer (Uniform Distribution)

---

# 🧪 Total Experiments Performed

The project performs a total of **23 clustering iterations**.

## K-Means Experiments (7)
1. KMeans + Raw Data
2. KMeans + StandardScaler
3. KMeans + RobustScaler
4. KMeans + MinMaxScaler
5. KMeans + PowerTransformer (Yeo-Johnson)
6. KMeans + PowerTransformer (Box-Cox)
7. KMeans + QuantileTransformer

---

## GMM Experiments (16)

### StandardScaler
- GMM Full
- GMM Tied
- GMM Diag
- GMM Spherical

### RobustScaler
- GMM Full
- GMM Tied
- GMM Diag
- GMM Spherical

### MinMaxScaler
- GMM Full
- GMM Tied
- GMM Diag
- GMM Spherical

### PowerTransformer (Yeo-Johnson)
- GMM Full
- GMM Tied
- GMM Diag
- GMM Spherical

---

# 📊 Evaluation Metrics

The clustering performance was evaluated using:

- Silhouette Score
- Cluster Distribution
- AIC (for GMM)
- BIC (for GMM)
- Log Likelihood (for GMM)

---

# 🏆 Best Iteration Selection

After running all clustering experiments, the best iteration is selected manually based on:
- Highest silhouette score
- Better cluster separation
- Balanced cluster distribution
- Business interpretability

The selected model is then used for:
- Final cluster assignment
- Persona creation
- User profiling

---

# 📌 Cluster Profiling Insights

## Cluster Size
- All four clusters were reasonably balanced
- No extremely dominant or very small cluster observed

## Age Distribution
- Most users belonged to the mid-20s to mid-30s age range
- Segmentation was behavior-driven rather than age-driven

## Subscription Tenure
- Similar tenure distribution across clusters
- Variations mainly reflected listening intensity and engagement

## Device Usage
- Mobile devices dominated across all clusters
- Desktop and tablet usage remained secondary

## Geographical Distribution
- Brazil and India represented the largest user groups
- UK, Denmark, and the US also showed consistent representation
- Geographic distribution remained relatively balanced across clusters

Each cluster was interpreted as a different user persona category.

---

# 🎭 Final Persona Summaries

Based on behavioral clustering and profiling analysis, four major Spotify user personas were identified.

---

## 🎧 Persona 1 — Casual Snackers

### Listening Pattern
- Low–medium listening intensity
- Short listening sessions
- Medium skip behavior

### User Description
Occasional listeners who mostly use music as background entertainment.

### Business Impact
- Low revenue potential
- Moderate retention
- Passive engagement behavior

### Recommended Strategy
- Soft nudges
- Trending playlists
- Frictionless user experience

---

## 🔍 Persona 2 — Exploratory Samplers

### Listening Pattern
- Medium intensity
- High listening frequency
- Medium–high skip rate

### User Description
Users who frequently explore new genres, artists, and mood-based playlists.

### Business Impact
- High discovery value
- Potential churn risk
- Strong recommendation dependency

### Recommended Strategy
- AI-based recommendations
- Genre discovery systems
- Personalized onboarding

---

## 🎵 Persona 3 — Habitual Loyalists

### Listening Pattern
- Medium–high intensity
- High consistency
- Long listening sessions

### User Description
Users with stable routine-based listening behavior and strong platform loyalty.

### Business Impact
- High lifetime value (LTV)
- Strong retention
- Monetization sweet spot

### Recommended Strategy
- Premium upselling
- Daily playlists
- Loyalty rewards

---

## 🔥 Persona 4 — Power Streamers

### Listening Pattern
- Highest listening intensity
- Longest session durations
- Lowest skip behavior

### User Description
Highly engaged music consumers deeply connected with the platform.

### Business Impact
- Highest premium conversion potential
- Strong engagement drivers
- Revenue-focused user base

### Recommended Strategy
- Hi-Fi audio
- Exclusive content
- Advanced personalization

---

# 📌 Cluster Profiling Insights

## Cluster Size
- All four clusters were reasonably balanced
- No extremely dominant or very small cluster observed

## Age Distribution
- Most users belonged to the mid-20s to mid-30s age range
- Segmentation was behavior-driven rather than age-driven

## Subscription Tenure
- Similar tenure distribution across clusters
- Variations mainly reflected listening intensity and engagement

## Device Usage
- Mobile devices dominated across all clusters
- Desktop and tablet usage remained secondary

## Geographical Distribution
- Brazil and India represented the largest user groups
- UK, Denmark, and the US also showed consistent representation
- Geographic distribution remained relatively balanced across clusters

# 📈 Visualizations Included

The project generates multiple visualizations:

- Cluster Size Distribution
- Age Distribution by Cluster
- Subscription Tenure Distribution
- Device Type Distribution
- Country Distribution
- Heatmaps for Cluster Profiling

---

# 📁 Project Workflow

```text
1. Load Data
2. Feature Selection
3. Data Preprocessing
4. Run 23 Clustering Experiments
5. Evaluate Models
6. Select Best Iteration
7. Assign Final Clusters
8. Perform Cluster Profiling
9. Generate Personas
10. Visualize Insights