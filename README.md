Markdown
# 🔬 Pan-European CS Research Trends: Automated Literature Mining via OpenAlex API & NLP

An end-to-end data pipeline that extracts, cleans, flattens, and analyzes recent Computer Science research output across top European academic hubs (Netherlands & Finland) using the OpenAlex REST API and Natural Language Processing (NLP).

---

## 📌 Project Overview
Instead of relying on static CSV files or manual literature searches, this project automates the academic literature review process. By interfacing directly with the **OpenAlex API**, this pipeline retrieves real-time publication metadata from Dutch and Finnish institutions, reconstructs inverted abstract indices into full readable text, and applies text-mining techniques to surface trending research topics.

This project demonstrates practical competence in consuming REST APIs, handling complex nested JSON objects, writing custom text reconstruction algorithms, and performing exploratory NLP text analysis.

---

## 🔑 Key Technical Highlights
* **REST API Integration & Error Handling:** Interfaced with the OpenAlex API using custom request parameters, polite pool identification (`mailto`), and graceful handling for HTTP status codes (such as `429 Rate Limits`).
* **Algorithmic Abstract Reconstruction:** OpenAlex stores abstracts as an inverted positional index (`{"word": [0, 5]}`) to comply with copyright laws. Designed an algorithm to reconstruct these indices into complete, ordered text paragraphs.
* **NLP & Text Mining:** Applied Regular Expressions (`re`) to clean text, normalized terms, filtered out domain-specific stop words, and calculated term frequencies using `Counter`.
* **Exploratory Data Analysis:** Built visualizations comparing keyword frequencies across publications and analyzed abstract length distributions between institutions.

---

## 🛠️ Tech Stack & Tools
* **Language:** Python 3.x
* **API Requests:** `requests`, REST API (OpenAlex)
* **Data Processing & Engineering:** `pandas`, `re` (Regular Expressions), `collections.Counter`
* **Visualization:** `seaborn`, `matplotlib`
* **Environment:** Google Colab

---

## 📊 Key Insights & Visualizations

### 1. Trending CS Keywords
Identified high-frequency research topics across recent Computer Science publications originating from Netherlands and Finland research groups.

### 2. Abstract Length Distribution
Analyzed the word-count density of research abstracts using stacked histograms to compare publication detail levels across different countries.

---

## 📁 Repository Structure
├── openalex_nlp_pipeline.py            # Complete Python script (API + Processing + Viz)
├── dutch_finnish_cs_research_trends.csv# Cleaned dataset with reconstructed abstracts
├── research_keyword_trends.png          # Bar chart visualization output
├── abstract_length_histogram.png        # Stacked histogram output
└── README.md                            # Technical documentation


---

## ⚙️ How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/dutch-finnish-cs-research-trends-nlp.git](https://github.com/YOUR_USERNAME/dutch-finnish-cs-research-trends-nlp.git)
Install dependencies:

Bash
pip install pandas requests matplotlib seaborn
Configure API Access:
Open openalex_nlp_pipeline.py and update the mailto field with your email address to enter the OpenAlex Polite Pool:

Python
"mailto": "your_email@example.com"
Execute the script:

Bash
python openalex_nlp_pipeline.py
