# Public Sentiment Mining on Nikola Motors Using Social Media Data

## 📌 Purpose
This project analyzes public sentiment and trending topics surrounding **Nikola Motors**, using user-generated content from **Reddit** and **YouTube**. By applying techniques such as web scraping, NLP preprocessing, **topic modeling (LDA)**, and **sentiment analysis (VADER)**, this project helps understand how the EV brand is perceived online, especially during controversial events like the **Hindenburg report** and **Trevor Milton’s resignation**.

---

## 📂 Dataset Overview

The dataset includes social media comments collected using:
- **Reddit API**: Comments from discussions on Nikola Motors and related topics.
- **YouTube API**: Comments from relevant videos (e.g., news reports, reviews).
  
Each comment contains:
- Text content
- Author
- Platform (Reddit or YouTube)
- Date
- Metadata such as sentiment score, topic assignment

---

## 🔄 Steps & Implementation

### 🧹 Data Collection & Preprocessing
- Scraped data using Python APIs (Reddit & YouTube).
- Applied preprocessing steps:
  - Lowercasing, punctuation cleanup
  - URL & retweet removal
  - Language detection (filtered for English)
  - Kept only comments > 10 characters

### 📊 Exploratory Data Analysis (EDA)
- Bar charts of **top commenters**
- **Word frequency analysis** using Counter
- **Word cloud visualizations** of top terms

### 🧠 Topic Modeling - LDA
- Used **Gensim's LDA** on preprocessed comments
- Displayed most dominant keywords for each topic
- Evaluated using **Coherence Score** and **Perplexity**
- Visualized topic distributions across comments

### 😃 Sentiment Analysis
- Used **VADER** (from NLTK) to compute sentiment scores:
  - Positive
  - Neutral
  - Negative
- Visualized sentiment distributions using histograms

---

## 📈 Key Results

### 🧠 Topics Identified via LDA:
- Product performance
- Fraud accusations
- Executive leadership (Trevor Milton)
- Market sentiment & stock reaction

### 😡 Sentiment Trends:
- Dominantly **negative sentiment**
- High public skepticism around fraud allegations
- Peaks in negativity aligned with breaking news or legal updates

### 📢 Top Authors:
- Reddit users with high influence in discussions were identified
- Suggested a few key voices shaping the online narrative

---

## ⚙️ Installation

```bash
git clone https://github.com/Shiban1503/Nikola-Motors-Social-Analytics.git
cd Nikola-Motors-Social-Analytics
python -m venv venv
venv\Scripts\activate  # On Windows
pip install -r requirements.txt
```

## 📁 Project Structure
```
├── data/
│   └── combined_comments.csv        # Cleaned data
├── notebooks/
│   ├── 01_scraping.ipynb
│   ├── 02_eda.ipynb
│   └── 03_topic_sentiment.ipynb
├── visuals/
│   └── *.png                        # All plots and charts
├── requirements.txt
├── README.md
└── LICENSE
```
---
##⚠️ Disclaimer

This project works with Python 3.7 to 3.9.
VADER and Gensim are compatible with these versions. For Python 3.10+, minor updates to LDA parameters or tokenization libraries might be needed.
---
##🙌 Contributing

Contributions are welcome! Please:

Fork the repo

Create a new branch:
```
git checkout -b feature-name
```
Make changes and push:
```
git commit -m "Add feature"
git push origin feature-name
```
Submit a pull request
---
##📌 Conclusion

This project demonstrates how social media analytics can reveal public sentiment and conversation trends around controversial events involving corporate brands. Through Reddit and YouTube analysis, we gain actionable insights into trust erosion, crisis reactions, and brand perception. Businesses and PR teams can use this approach to monitor and respond to digital reputation in real-time.
