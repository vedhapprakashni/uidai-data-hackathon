# Aadhaar Enrollment Analysis & Desert Identification

A comprehensive data analysis project for identifying enrollment gaps and deserts in Aadhaar enrollment data across India, using machine learning clustering and multi-dimensional statistical analysis.

## 📋 Project Overview

This project analyzes Aadhaar enrollment data at multiple geographic levels (pincode, district, and state) to identify enrollment patterns, gaps, and critical "enrollment deserts" - areas with significantly low enrollment coverage that require intervention.

### Key Features

- **Multi-level Geographic Aggregation**: Analysis at pincode, district, and state levels
- **Comprehensive Statistical Analysis**: Univariate, bivariate, and trivariate analysis
- **Machine Learning Clustering**: K-Means, DBSCAN, and Hierarchical clustering
- **Desert Identification**: Custom Desert Identification Index (DII) to prioritize intervention areas
- **Geographic Optimization**: Optimal center placement recommendations using clustering
- **Predictive Modeling**: Early warning system for at-risk pincodes using Random Forest
- **Interactive Visualizations**: 29+ static and interactive visualizations using Matplotlib, Seaborn, and Plotly
- **Age Group Analysis**: Detailed breakdown by children (0-5), youth (5-17), and adults (18+)

## 🛠️ Technologies Used

- **Python**
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn, Plotly
- **Machine Learning**: Scikit-learn
- **Statistical Analysis**: SciPy

## 📊 Analysis Phases

### Phase 1: Setup & Data Loading
- Environment setup and library imports
- Data loading and initial exploration
- Basic dataset structure analysis

### Phase 2: Data Cleaning & Preprocessing
- Missing value handling
- Data type conversions
- Feature engineering (enrollment rates, temporal features, geographic indicators)
- Creation of urban/metro classifications

### Phase 3: Multi-Level Aggregation
- **Pincode-level**: Enrollment metrics, velocity, and duration
- **District-level**: Coverage density and demographic breakdowns
- **State-level**: High-level enrollment summaries and comparisons

### Phase 4: Univariate Analysis
- Enrollment distribution analysis
- Geographic coverage metrics
- Age group distribution
- Temporal enrollment trends
- Top/bottom performing regions

### Phase 5: Bivariate Analysis
- Geography vs enrollment relationships
- Time vs enrollment patterns
- Demographics vs geography correlations
- Day-of-week enrollment analysis
- State-district heatmaps

### Phase 6: Trivariate Analysis
- 3D scatter plots (child rate × enrollments × velocity)
- Animated bubble charts showing temporal dynamics
- Hierarchical sunburst visualizations
- Multi-dimensional heatmaps
- Parallel coordinates analysis

### Phase 7: Machine Learning - Clustering
- **K-Means Clustering**: Optimal cluster identification using elbow method and silhouette scores
- **DBSCAN**: Density-based clustering for outlier detection
- **Hierarchical Clustering**: Dendrogram visualization
- Cluster profiling and naming (e.g., "High Coverage Metro Areas", "Critical Gaps")

### Phase 8: Enrollment Desert Identification
- Multi-criteria desert definition (OR logic: low enrollment OR low child rate OR critical cluster OR outlier)
- Desert Identification Index (DII) calculation with weighted components
- Severity categorization (Adequate, Moderate Concern, High Risk, Critical Desert)
- State-wise and district-wise desert analysis
- Priority intervention area identification
- Geographic mapping of desert severity

### Phase 9: Geographic Accessibility Optimization
- Existing center identification (top 10% by enrollment volume)
- Optimal new center placement using K-Means clustering
- Priority scoring for center locations (desert_index × pincodes_covered)
- Mobile camp route generation for remote areas
- Impact projection and coverage improvement calculations
- Recommendations for 25 new enrollment centers

### Phase 10: Predictive Modeling
- Random Forest Classifier for desert prediction
- Early warning system for at-risk pincodes
- Feature importance analysis
- Model evaluation metrics (accuracy, precision, recall, F1-score)
- Probability-based risk assessment
- Preventive intervention recommendations

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn scipy
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/uidai-hackathon.git
cd uidai-hackathon
```

2. Prepare your data files:
   - Place CSV files in the project directory
   - Ensure files are named as expected by the script

3. Run the analysis:
```bash
python uidai_hackathon.py
```

Or run in Google Colab:
- Upload the notebook to Google Colab
- Upload your CSV files when prompted
- Run all cells

## 📈 Output Files

### Aggregated Datasets
- `pincode_aggregated.csv`: Pincode-level enrollment metrics
- `district_aggregated.csv`: District-level summaries
- `state_aggregated.csv`: State-level aggregations

### Clustering Results
- `pincode_with_clusters.csv`: Pincodes with K-Means and DBSCAN cluster assignments

### Desert Identification
- `enrollment_deserts.csv`: All pincodes with desert severity scores and DII
- `critical_deserts.csv`: Filtered list of critical intervention areas (DII > 80)

### Optimization & Recommendations
- `recommended_centers.csv`: 25 new enrollment center locations with priority rankings

### Predictive Modeling
- `at_risk_pincodes.csv`: Pincodes at risk of becoming deserts (early warning list)

### Visualizations (29+ files)
- Static PNG images (26+ files): Distributions, heatmaps, cluster plots, desert maps
- Interactive HTML files (3+ files): 3D scatter plots, animated charts, sunburst hierarchies

## 🎯 Key Insights & Metrics

### Desert Identification Index (DII)
Calculated using weighted components:
- **Enrollment Score** (30%): Overall enrollment performance
- **Child Coverage Score** (30%): Focus on children (0-5)
- **Velocity Score** (20%): Enrollment rate/speed
- **Cluster Risk Score** (20%): ML-based risk assessment

### Severity Categories
- **Adequate**: DII 0-40 (No immediate concern)
- **Moderate Concern**: DII 40-60 (Monitor)
- **High Risk**: DII 60-80 (Intervention recommended)
- **Critical Desert**: DII 80-100 (Urgent intervention required)

## 📊 Sample Visualizations

The project generates comprehensive visualizations including:
- **Univariate Analysis:** Distribution histograms, box plots, pie charts, bar charts
- **Bivariate Analysis:** Scatter plots, correlation matrices, state-district heatmaps
- **Trivariate Analysis:** 3D scatter plots, animated bubble charts, hierarchical sunburst
- **Clustering:** Cluster profiles, dendrograms, scatter plots with cluster assignments
- **Desert Identification:** Severity maps, state-wise summaries, priority rankings
- **Optimization:** Center location maps, coverage improvement charts
- **Predictive Modeling:** Feature importance plots, model performance metrics

## 📈 Project Statistics

### Data Processed
- **Total Records:** 1,000,000 (raw) → 993,964 (clean)
- **Geographic Coverage:** 30,359 pincodes across 1,095 districts in 63 states/UTs
- **Time Period:** January 2025 - December 2025
- **Total Enrollments Analyzed:** 3,273,755

### Key Findings
- **Zero Enrollment Pincodes:** 2,587 (8.5% of total)
- **Average Enrollment per Pincode:** 107.83
- **Top State:** Uttar Pradesh (663,768 enrollments, 20.3% of total)
- **Age Distribution:** 61.1% children (0-5), 35.1% youth (5-17), 3.7% adults (18+)
- **Metro vs Non-Metro:** Metro pincodes average 22% higher enrollments (131 vs 107)

### Analysis Outputs
- **Aggregated Datasets:** 3 files (pincode, district, state levels)
- **ML Results:** 1 file (clusters)
- **Desert Analysis:** 2 files (all deserts, critical deserts)
- **Optimization:** 1 file (recommended centers)
- **Predictions:** 1 file (at-risk pincodes)
- **Visualizations:** 29+ files (static and interactive)

## 🎯 Use Cases

This analysis supports:
1. **Resource Allocation:** Prioritize enrollment center deployment based on data
2. **Intervention Planning:** Identify and target critical enrollment deserts
3. **Policy Development:** Evidence-based enrollment drive strategies
4. **Monitoring:** Early warning system for at-risk areas
5. **Optimization:** Cost-effective center placement recommendations

## 🔧 Technical Implementation

### Machine Learning Models
- **K-Means Clustering:** Groups similar enrollment patterns (optimal K via silhouette score)
- **DBSCAN:** Detects outliers and anomalous pincodes
- **Random Forest Classifier:** Predicts desert risk with balanced class weights
- **Hierarchical Clustering:** Validates cluster structures

### Key Algorithms
- **Desert Identification Index:** Weighted composite score (30% + 30% + 20% + 20%)
- **Priority Scoring:** `desert_index × pincodes_covered` for center recommendations
- **Feature Engineering:** 15+ derived features including rates, velocities, percentiles

## 📝 Project Status

✅ **All 10 Phases Complete:**
- ✅ Phase 1: Setup & Data Loading
- ✅ Phase 2: Data Cleaning & Preprocessing
- ✅ Phase 3: Multi-Level Aggregation
- ✅ Phase 4: Univariate Analysis
- ✅ Phase 5: Bivariate Analysis
- ✅ Phase 6: Trivariate Analysis
- ✅ Phase 7: Machine Learning - Clustering
- ✅ Phase 8: Enrollment Desert Identification
- ✅ Phase 9: Geographic Accessibility Optimization
- ✅ Phase 10: Predictive Modeling

## 📚 Documentation

Additional documentation available:
- `PHASE_REPORT.md`: Detailed phase-by-phase implementation report
- `PROJECT_REPORT.md`: Comprehensive 15-20 page project report
- `CODE_REVIEW_PHASES_7-10.md`: Technical review of ML implementation
- `SIMPLEST_EXPLANATION.md`: Simple explanations of complex concepts

## 🤝 Contributing

This project was developed for the UIDAI Data Hackathon. For questions or contributions, please refer to the project documentation.

## 📄 License

This project is part of the UIDAI Data Hackathon submission.

---

**Note:** This project uses enrollment data provided by UIDAI. All analysis and insights are for research and decision-support purposes. Add screenshots of key visualizations when preparing the final PDF submission.
