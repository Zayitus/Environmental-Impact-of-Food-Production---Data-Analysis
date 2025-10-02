A comprehensive exploratory data analysis of greenhouse gas emissions, land use, and water footprint across 43 food products.# 🌍 Environmental Impact of Food Production - Data Analysis

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF.svg)](https://www.kaggle.com/datasets/selfvivek/environment-impact-of-food-production)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> A comprehensive exploratory data analysis of greenhouse gas emissions, land use, and water footprint across 43 food products.

---

## 📋 Table of Contents
- [Overview](#-overview)
- [Key Findings](#-key-findings)
- [Technologies](#-technologies)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [Methodology](#-methodology)
- [Results & Visualizations](#-results--visualizations)
- [Conclusions](#-conclusions)
- [Future Work](#-future-work)
- [Contact](#-contact)

---

## 🎯 Overview

This project analyzes the environmental impact of food production using data from Kaggle's "Environment Impact of Food Production" dataset. The analysis explores:

- **Greenhouse gas emissions** (kg CO₂eq per kg product)
- **Land use** (m² per kg product)
- **Freshwater withdrawals** (liters per kg product)
- **Eutrophying emissions** (g PO₄eq per kg product)
- **Production stage breakdown** (Farm, Processing, Transport, Packaging, Retail)

### Objectives
1. Compare environmental impacts between animal-based and plant-based foods
2. Identify outliers and high-impact products
3. Analyze correlations between environmental metrics
4. Apply clustering techniques to group similar food products
5. Provide actionable recommendations for sustainable dietary choices

---

## 🔑 Key Findings

### 🥩 vs 🌱 Animal vs Plant-Based Foods

| Metric | Animal-Based | Plant-Based | Difference |
|--------|--------------|-------------|------------|
| **Median GHG Emissions** | 7.6 kg CO₂eq | 1.2 kg CO₂eq | **6.4x higher** |
| **Statistical Significance** | Mann-Whitney U test: *p* = 0.003 | ✅ Significant |
| **Emissions Range** | 1.0 – 59.6 kg CO₂eq | 0.9 – 4.0 kg CO₂eq | - |

### 🔥 Top Environmental Impact Foods

1. **Beef (beef herd)**: 59.6 kg CO₂eq - *Highest-impact food*
2. **Lamb & Mutton**: 24.5 kg CO₂eq
3. **Beef (dairy herd)**: 21.1 kg CO₂eq
4. **Cheese**: 21.2 kg CO₂eq
5. **Farmed Fish**: 13.6 kg CO₂eq

### 🌿 Low Impact Alternatives

- **Legumes** (beans, lentils, peas): ~1.0 kg CO₂eq
- **Soy products** (tofu, soymilk): ~1.0 kg CO₂eq
- **Grains** (wheat, barley): ~1.4 kg CO₂eq
- **Poultry** (if consuming animal products): 6.1 kg CO₂eq

### 💡 Impact of Dietary Shifts

- Replacing **beef → poultry**: **90% reduction** in GHG emissions
- Replacing **beef → legumes**: **97% reduction** in GHG emissions
- Adopting a **flexitarian diet**: **30-50% reduction** in footprint

---

## 🛠 Technologies

**Programming & Analysis:**
- Python 3.8+
- Pandas (data manipulation)
- NumPy (numerical computing)
- SciPy (statistical tests)

**Visualization:**
- Matplotlib
- Seaborn
- Plotly (interactive plots)

**Machine Learning:**
- Scikit-learn (clustering, preprocessing)
- K-means clustering

**Environment:**
- Jupyter Notebook
- Google Colab
- Kaggle API

---

## 📁 Project Structure

```
food-sustainability-analysis/
│
├── README.md                          # Project documentation
├── food_sustainability_analysis.ipynb # Main Jupyter notebook
├── requirements.txt                   # Python dependencies
├── LICENSE                            # MIT License
│
├── data/
│   └── Food_Production.csv           # Dataset (from Kaggle)
│
└── images/
    ├── ghg_comparison.png            # Key visualizations
    ├── correlation_heatmap.png
    └── clustering_results.png
```

---

## 💻 Installation

### 1. Clone the repository
```bash
git clone https://github.com/[your-username]/food-sustainability-analysis.git
cd food-sustainability-analysis
```

### 2. Create a virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up Kaggle API (for dataset download)
- Create a Kaggle account
- Go to Account Settings → API → "Create New API Token"
- Place `kaggle.json` in `~/.kaggle/` (Linux/Mac) or `C:\Users\<Username>\.kaggle\` (Windows)

---

## 🚀 Usage

### Option 1: Run Locally
```bash
jupyter notebook food_sustainability_analysis.ipynb
```

### Option 2: Run on Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/[your-username]/food-sustainability-analysis/blob/main/food_sustainability_analysis.ipynb)

### Option 3: View on Kaggle
[View Notebook on Kaggle](https://www.kaggle.com/code/[your-kaggle-username]/food-sustainability-analysis)

---

## 🔬 Methodology

### 1. **Data Loading & Cleaning**
- Dataset: 43 food products with 23 environmental metrics
- Handling missing values (especially in protein-normalized metrics)
- Data validation and type conversion

### 2. **Exploratory Data Analysis (EDA)**
- Descriptive statistics
- Distribution analysis
- Outlier detection (IQR method)

### 3. **Comparative Analysis**
- Animal vs plant-based foods
- Statistical testing (Mann-Whitney U test)
- Breakdown by production stage

### 4. **Correlation Analysis**
- Pearson correlation coefficients
- Heatmap visualizations
- Multi-dimensional relationships

### 5. **Clustering**
- K-means algorithm (k=3)
- Silhouette score optimization
- Impact group identification

### 6. **Visualization**
- Boxplots, bar charts, scatter plots
- Interactive visualizations
- Trade-off analysis

---

## 📊 Results & Visualizations

### Production Stage Contribution
- **Farm stage**: ~52% of total emissions (dominant factor)
- **Animal feed**: 15.8% for animal products
- **Transport & Packaging**: More relevant for plant-based foods

### Environmental Correlations
| Metric Pair | Correlation (ρ) | Strength |
|-------------|-----------------|----------|
| GHG ↔ Eutrophication | 0.85 | Very Strong |
| GHG ↔ Land Use | 0.81 | Strong |
| GHG ↔ Water Use | 0.54 | Moderate |

### Clustering Results
- **Cluster 1 (Low Impact)**: 28 foods, avg 3.1 kg CO₂eq
- **Cluster 2 (Medium Impact)**: 8 foods, avg 8.4 kg CO₂eq
- **Cluster 3 (High Impact)**: 2 foods, avg 42.1 kg CO₂eq

---

## 🎓 Conclusions

### Main Takeaways
1. **Animal-based foods have 6.4x higher emissions** than plant-based alternatives
2. **Beef is the highest-impact food**, contributing 10-30x more emissions than plant alternatives
3. **Farm stage is the critical intervention point** (52% of emissions)
4. **Poultry and legumes** are the most sustainable protein sources

### Practical Recommendations

**🟢 Low Impact (Prioritize):**
- Legumes, grains, soy products, nuts

**🟡 Medium Impact (Moderate):**
- Rice, poultry, farmed fish

**🔴 High Impact (Reduce/Avoid):**
- Beef, lamb, cheese

### Policy Implications
- Carbon taxes on high-impact foods
- Subsidies for plant-based protein production
- Consumer education campaigns

---

## 🚀 Future Work

- [ ] Expand dataset with more products and regional variations
- [ ] Incorporate full life-cycle assessment (LCA)
- [ ] Add nutritional dimension (impact per nutrient)
- [ ] Model population-level dietary shift scenarios
- [ ] Develop an interactive web dashboard
- [ ] Integrate economic accessibility analysis

---

## 📚 References

- Dataset: [Kaggle - Environment Impact of Food Production](https://www.kaggle.com/datasets/selfvivek/environment-impact-of-food-production)
- Poore, J., & Nemecek, T. (2018). *Reducing food's environmental impacts through producers and consumers*. Science, 360(6392), 987-992.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👤 Contact

**[Your Name]**

- 🌐 Portfolio: [your-website.com]
- 💼 LinkedIn: [linkedin.com/in/your-profile]
- 🐙 GitHub: [github.com/your-username]
- 📧 Email: your.email@example.com

---

⭐ **If you found this project helpful, please consider giving it a star!** ⭐

---

*Last updated: October 2024*
