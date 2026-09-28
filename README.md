# Social Media Engagement Analytics using Python

### Project Done By: ABIRAMI GANESAN

## 📌 Project Overview
This project focuses on the end-to-end data analytics lifecycle of a social media dataset containing **5,000 unique posts**. Using robust statistical methods and dynamic data visualizations, the project transforms raw metrics (likes, comments, shares, impressions, watch time) into highly actionable business strategies. 

The analysis reveals critical audience behavior patterns, uncovers hidden core relationships (such as the "Viral Dilution Effect"), and details how content types and geographical demographics influence overall platform traction.

---

## 🛠️ Project Architecture & Pipeline

### Task 1 — Data Import & Setup
* Loaded the raw 5,000-row transaction dataset using `pandas.read_csv()`.
* Structured structural data pipelines and converted temporal tracking logs (`posted_at`) into explicit `datetime64` format.

### Task 2 — Data Cleaning & Outlier Management
* **Missing Value Imputation:** Handled missing numerical columns (`age`, `likes`, `comments`, `shares`) cleanly with global `mean` metrics. Categorical features like `sentiment` were filled with `'Unknown'` placeholders, and `gender` gaps were resolved via statistical `mode` injection.
* **Structural Text Alignment:** Standardized objective categorization columns by stripping empty string spaces and applying capitalization rules.
* **Advanced Outlier Mitigation:** Identified deep, right-skewed anomalies in `engagement_rate` via distribution box plots and KDE histograms. Used the **Capping Method** via Upper Bounds to compress extreme values without losing 36% of the data, keeping the dataset intact at 5,000 complete records.

### Task 3 — Exploratory Data Analysis (EDA)
* Extracted core matrix layouts using structural descriptive stats (`.describe()`, `.info()`, and `.shape`).
* Deployed deep Pandas Multi-Index `.groupby()` mechanics to isolate cross-categorical data behaviors across demographics, devices, sentiments, and geographies.

### Task 4 — Data Wrangling & Feature Engineering
* Built calculated fields to measure audience engagement characteristics, including `hashtag_count` extracted directly from clean raw hashtag strings.
* Engineered an explicit structural segmentation column (`age_level`) by binning age distributions into `Teen`, `Young Adult`, `Middle Aged`, and `Senior` classifications.

### Task 5 — Statistical Profiling
* Evaluated high-level skewness and kurtosis metrics over all continuous vectors to mathematically define system normalcy boundaries.

### Task 6 — Advanced Visualizations
Constructed a data storytelling portfolio using 3 separate plotting frameworks:
* **Matplotlib:** Created structured Scatter Plots (Reach vs Likes), Chronological Line Trends, Category Bar Distortions, Gender Distribution Pie Maps, and Demographic Histograms.
* **Seaborn:** Produced Category Count Plots, Multi-Chambered Category Bar Layouts, Sentiment Violin Splices, Pairplots, and Correlation Heatmaps.
* **Plotly Express:** Built clean interactive line charts tracking daily hourly watch times, multi-variable Bubble charts (Reach vs Engagement vs Volume by Country), and multi-colored feature scatter maps.

---

## 🗂️ Repository Structure

```text
├── Social_Media_Engagement_Analytics.ipynb   # Main documented Google Colab Notebook
├── README.md                                 # Technical project documentation
└── requirements.txt                          # Python execution dependencies
```

---

## 🚀 Getting Started

### Prerequisites
Ensure your local environment has Python 3.8+ installed.

### Installation
1. Clone this repository to your machine:
   ```bash
   git clone https://github.com
   cd social-media-analytics
   ```

2. Install the necessary analysis libraries:
   ```bash
   pip install -r requirements.txt
   ```
   *(Or manually run: `pip install numpy pandas matplotlib seaborn plotly`)*

### Execution
Open the notebook in your preferred environment:
```bash
jupyter notebook Social_Media_Engagement_Analytics.ipynb
```

---

## 🧰 Tech Stack
* **Language:** Python 3
* **Data Processing & Wrangling:** Pandas, NumPy
* **Static Visualization Architecture:** Matplotlib, Seaborn
* **Interactive Visualization Engine:** Plotly Express
* **Environment:** Jupyter Notebook / Google Colab

## 🔬 Core Analysis & Key Insights

The project utilizes a 4-tier analytical framework to turn raw data into strategic execution:

### 1. Descriptive Analysis (What Happened?)
* **Core Demographics:** The platform's primary consumer cluster resides within the **35–45 age bracket** (Middle-Aged & Young Adults), showing an evenly split gender distribution.
* **Device Agnosticism:** Media consumption habits are identical across screens. Mobile, Tablet, and Desktop architectures capture equivalent watch times and exhibit heavily mirrored engagement patterns.
* **Temporal Patterns:** Algorithmic reach and user posting distributions remain steady throughout the week. Visibility peaks mildly on **Tuesdays**, followed closely by **Mondays** and **Saturdays**.
* **Engagement Standards:** After removing extreme mathematical outliers, a healthy baseline engagement rate on this platform hovers predictably between **0.0 and 0.4**.

### 2. Diagnostic Analysis (Why Did It Happen?)
* **The "Viral Dilution" Effect:** A critical, extremely strong negative correlation (**r = -0.95**) exists between `impression_count` and `engagement_rate`. As the recommendation engine pushes content to a massive, passive audience, the percentage of active interactors drops drastically.
* **Geographical Divergence:** 
  * **India** serves as a megaphone: It commands the highest raw impressions but the lowest quality interaction rate (~0.35).
  * **Australia** behaves as a highly dedicated community: It records the lowest structural reach but produces the absolute highest engagement rate (~0.415).
* **Content Psychology:**
  * **Fitness** content drives massive, organic **shares** but low likes, as users treat posts as resource-driven assets to forward to peers.
  * **Music** commands the highest cumulative **watch time** due to background-listening behaviors.
  * **Lifestyle** content structurally underperforms across all primary interaction layers.

### 3. Predictive Analysis (What Will Happen Next?)
* **Algorithmic Equality:** The statistical relationship between viewer age and raw reach is effectively flat (**r = 0.017**). Future impressions will be driven strictly by content-trend velocity rather than demographic targeting.
* **Interaction Projections:** Direct optimizations toward capturing "likes" will mathematically yield a direct, reliable lift in total engagement matrices due to a resilient positive correlation (**r = +0.51**).
* **Niche Performance Forecasts:** Scaling Fitness content guarantees a surge in shared networks, while continued investment in Lifestyle content will result in decaying channel traction.

### 4. Prescriptive Analysis (How Should We Act?)
* **Bifurcated Regional Campaigns:** Run broad brand-awareness and top-of-funnel reach campaigns in India. Target bottom-of-funnel direct actions, conversions, and high-value pitches in Australia.
* **Strategic Content Matching:** 
  * Deploy **Fitness** content to stimulate community virality and peer-to-peer sharing.
  * Utilize **Music/Audio** formats to maximize user watch-time retention metrics.
  * Benchmark **Tech** content to ensure a reliable balance between steady likes and shared networks.
* **Resource Optimization:** Discontinue spending creative hours designing device-specific structural formats or strictly timing weekend publication hour thresholds. The data proves platform audiences interact uniformly across all days and devices.

### 🏁 Conclusion

  This project successfully demonstrated an end-to-end data analytics architecture that transformed 5,000 raw social media records into actionable business strategies. By building robust data cleaning and pipeline workflows in Pandas—handling null values via mean/mode imputation, standardizing category labels, and controlling extreme right-skewed anomalies using custom capping methods—we ensured 100% data preservation and integrity for the final models. Through strategic feature engineering and multidimensional Pandas groupby aggregations, we successfully uncovered deep behavioral trends across demographics, formats, and devices. Finally, by mapping these relationships out through an exhaustive visualization suite in Matplotlib, Seaborn, and Plotly, this project successfully delivered concrete diagnostic insights—such as the viral reach dilution effect—providing a reliable framework for data-driven content optimization and marketing strategy going forward.

---
