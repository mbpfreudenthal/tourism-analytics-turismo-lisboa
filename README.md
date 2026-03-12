# 🗺️ Tourism Analytics — Turismo de Lisboa
### Data Science for Marketing | NOVA IMS | Group 10

> *Transforming 100k+ TripAdvisor reviews into actionable intelligence for Lisbon's Tourism Authority*

---

## 📌 Project Overview

This project was developed for **Turismo de Lisboa (LTA)** — the authority responsible for promoting Lisbon as a high-quality, competitive, and sustainable tourist destination.

**The business problem:** TripAdvisor reviews are rich in insight but largely unstructured, making them difficult to translate into actionable marketing and management decisions.

**Our solution:** A full end-to-end CRISP-DM pipeline combining NLP, behavioural segmentation, similarity analysis, and statistical validation to extract actionable signals from visitor review data.

---

## 🎯 Business Questions Answered

| # | Question | Method |
|---|----------|--------|
| 1 | Can sentiment in reviews predict future ratings? | Spearman Correlation (H1) |
| 2 | Does crowding reduce visitor satisfaction? | Mann–Whitney U Test (H2) |
| 3 | Which reviewers are most valuable/at risk? | RFM Segmentation |
| 4 | Which attractions are most similar to each other? | Cosine Similarity |
| 5 | Which attractions are visited together? | Market Basket / Apriori |

---

## 🔬 Methodology — CRISP-DM

```
1. Business Understanding  →  LTA goals, KPIs, campaign strategy context
2. Data Understanding      →  3 datasets merged (reviews, metadata, attractions)
3. Data Preparation        →  Cleaning, feature engineering, text mining (NLP)
4. Modelling & Analysis    →  RFM, similarity measures, market basket analysis
5. Evaluation              →  Hypothesis testing, sanity checks, robustness
6. Conclusions             →  Validated framework ready for deployment
```

---

## 🧰 Tech Stack

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-NLP-green?style=flat)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Viz-blue?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-Viz-9cf?style=flat)

**Libraries:** `pandas` · `numpy` · `scikit-learn` · `nltk` · `langdetect` · `mlxtend` · `matplotlib` · `seaborn` · `joypy` · `squarify`

---

## 📊 Key Results

### 🔵 RFM Segmentation
Reviewers were segmented into behavioural groups (Champions, Loyal, At Risk, Lost, etc.) enabling targeted campaign strategies:
- **Champions** → Referral & ambassador programmes
- **At Risk** → Re-engagement campaigns with personalised offers
- **Lost** → Reactivation campaigns targeting previously popular attractions

### 🔵 Hypothesis Testing
- **H1 confirmed** ✅ — Sentiment is a statistically significant early-warning signal for rating changes (Spearman correlation, p < 0.05)
- **H2 confirmed** ✅ — Attractions with frequent crowding complaints receive significantly lower ratings during peak season (Mann–Whitney U, p < 0.05)

### 🔵 Similarity & Recommendation
- Built an attraction similarity engine using cosine similarity on aggregated review profiles
- Produced personalised top-5 attraction recommendations for individual reviewers based on visiting history

### 🔵 Market Basket Analysis
- Applied Apriori algorithm to identify attractions frequently co-visited
- Generated association rules to support bundled marketing and itinerary recommendations

---

## 📁 Repository Structure

```
tourism-analytics-turismo-lisboa/
│
├── notebooks/
│   └── Notebook_Group_10.ipynb       # Full analysis notebook
│
├── reports/
│   └── Report_Group_10.pdf           # Full written report
│
├── data/
│   └── README.md                     # Dataset description (data not included — see below)
│
└── README.md
```

> **⚠️ Data Note:** The raw datasets (TripAdvisor reviews, attraction metadata) are not included in this repository as they were provided under academic licence. The notebook is fully documented and reproducible with equivalent data.

---

## 👥 Team

| Name | Student ID |
|------|-----------|
| Beatriz Santos | 20221937 |
| Bernardo Teixeira | 20250831 |
| **Manuel Freudenthal** | **20250835** |
| Maria Inês Castro | 20221842 |

**Course:** Data Science for Marketing — MSc in Data Science for Marketing, NOVA IMS, Lisbon

---

## 🚀 How to Run

1. Clone the repo
   ```bash
   git clone https://github.com/YOUR_USERNAME/tourism-analytics-turismo-lisboa.git
   ```

2. Install dependencies
   ```bash
   pip install pandas numpy scikit-learn nltk langdetect mlxtend matplotlib seaborn joypy squarify
   ```

3. Open the notebook
   ```bash
   jupyter notebook notebooks/Notebook_Group_10.ipynb
   ```

> The notebook was originally developed in Google Colab. Update the `path` variable in Section 0 to point to your local data directory.

---

## 📬 Contact

**Manuel Freudenthal** · [LinkedIn](https://www.linkedin.com/in/manuel-freudenthal) · mbpfreudenthal@gmail.com
