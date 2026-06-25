# 📢 Ad Engagement & Customer Satisfaction Analysis

> **Type:** EDA · Funnel Analysis · Campaign Analytics · Demographic Segmentation
> 
> **Tools:** Python · Pandas · Matplotlib · Seaborn
> 
> **Dataset:** [Social Media Advertisement Performance](https://www.kaggle.com/datasets) — 4 tables: Users, Ads, Campaigns, Ad Events

---

## 🏢 Business Problem

A digital marketing team running campaigns across **Facebook and Instagram** had strong impression numbers — but poor clicks, conversions, and engagement. The core questions:

- Where exactly in the funnel are users dropping off?
- Is the targeting strategy reaching the right people?
- Which platform and ad format delivers the best value?

---

## 📐 Approach

| Step | What I Did |
|------|-----------|
| **Data Engineering** | Merged 4 raw tables (Users, Ads, Campaigns, Ad Events) into one unified dataset using outer joins on `campaign_id`, `ad_id`, `user_id` |
| **Data Cleaning** | Dropped rows with missing critical IDs; imputed remaining nulls — median for numeric columns, mode for categorical |
| **Funnel Analysis** | Computed drop-off ratio at each stage: Impression → Click → Like → Purchase → Share |
| **Targeting Audit** | Cross-matched `target_gender` + `target_age_group` vs actual `user_gender` + `age_group` of engaged users |
| **Platform Breakdown** | Pivot tables across country, age group, gender, ad format, platform — visualised as multi-panel bar charts |
| **Cost Efficiency** | Calculated cost-per-event per campaign (`total_budget / total_events`) |

---

## 📊 Key Findings

- **Impressions dominated** all event types — but conversion rates were very low → reach is not the problem, relevance is
- **Targeting misalignment:** most engaged users did NOT match the intended demographic — a gap invisible without cross-source analysis
- **Facebook** led in total volume; **Instagram Stories** outperformed in the 25–34 age group
- Engagement was **uniform across all time slots** — scheduling optimisation alone won't fix performance

---

## 💡 Business Recommendation

> Retarget using the *actual* engaged user profile, not the assumed one. Shift budget toward Instagram Stories for 25–34 segments. Fix the audience brief before optimising creative.

---

## 📁 Repository Structure

```
ad-engagement-analysis/
│
├── notebook/
│   └── ad-engagement-customer-satisfaction-analysis.ipynb
│
├── images/                   ← save chart screenshots from Kaggle here
│   ├── funnel_chart.png
│   └── platform_breakdown.png
│
└── README.md
```

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/ad-engagement-analysis.git

# Install dependencies
pip install pandas matplotlib seaborn numpy

# Run the notebook
jupyter notebook notebook/ad-engagement-customer-satisfaction-analysis.ipynb
```

> 📎 Dataset source: [Social Media Advertisement Performance on Kaggle](https://www.kaggle.com/datasets/jsonlee/social-media-advertisement-performance)
