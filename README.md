# Aadhaar Enrollment Analysis & Desert Identification

A comprehensive data analysis project for identifying enrollment gaps and deserts in Aadhaar enrollment data across India, using machine learning clustering and multi-dimensional statistical analysis.

## 📋 Project Overview

This project analyzes Aadhaar enrollment data at multiple geographic levels (pincode, district, and state) to identify enrollment patterns, gaps, and critical "enrollment deserts" - areas with significantly low enrollment coverage that require intervention.

### Key Features

- **Multi-level Geographic Aggregation**: Analysis at pincode, district, and state levels
- **Comprehensive Statistical Analysis**: Univariate, bivariate, and trivariate analysis
- **Machine Learning Clustering**: K-Means, DBSCAN, and Hierarchical clustering
- **Desert Identification**: Custom Desert Identification Index (DII) to prioritize intervention areas
- **Interactive Visualizations**: 29+ static and interactive visualizations using Matplotlib, Seaborn, and Plotly
- **Age Group Analysis**: Detailed breakdown by children (0-5), youth (5-17), and adults (18+)

## 🛠️ Technologies Used

- **Python 3.x**
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
- Multi-criteria desert definition
- Desert Identification Index (DII) calculation
- Severity categorization (Adequate, Moderate Concern, High Risk, Critical Desert)
- State-wise desert analysis
- Priority intervention area identification

## 📁 Project Structure


uidai-hackathon/
│
├── uidai_hackathon.py          # Main analysis script
├── README.md                    # This file
│
├── data/                        # Input data (not included)
│   ├── api_data_aadhar_enrolment_0_500000.csv
│   └── api_data_aadhar_demographic_500000_1000000.csv
│
├── figures/                     # Generated visualizations
│   ├── 01_enrollment_distributions.png
│   ├── 02_enrollment_boxplot_by_state.png
│   ├── ...
│   └── 29_desert_sunburst_map.html
│
└── outputs/                     # Generated datasets
    ├── pincode_aggregated.csv
    ├── district_aggregated.csv
    ├── state_aggregated.csv
    ├── pincode_with_clusters.csv
    ├── enrollment_deserts.csv
    └── critical_deserts.csv


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
- `enrollment_deserts.csv`: All pincodes with desert severity scores
- `critical_deserts.csv`: Filtered list of critical intervention areas

### Visualizations (29 files)
- Static PNG images (26 files)
- Interactive HTML files (3 files)

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
- Distribution histograms and box plots
- Geographic heatmaps
- Time series trends
- 3D scatter plots
- Animated bubble charts
- Cluster visualizations
- Desert severity maps
