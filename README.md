# Job Market Analysis 2024: Salary & Compensation Trends

A comprehensive data-driven analysis of job market trends, salary compensation, and the "AI wage premium" in 2024. This Quarto project leverages Python and PySpark to analyze 72,498 Lightcast job postings and uncover critical insights about the evolving job landscape.

**Authors:** Afreen Alam, Lo Ying Wu, Nutchanon Chaiyaratana, Tsyr Rau Chen  
**Date:** June 4, 2026  
**Course:** AD688 - Employability (Spring 2025)  
**Institution:** Boston University - Master of Science in Applied Business Analytics (MSABA)

---

## 📊 Project Overview

This project investigates key research questions in the modern job market:
- **The AI Impact**: How has artificial intelligence affected salary compensation and job demand?
- **Geographic Disparities**: Which regions command the highest salaries for AI and traditional roles?
- **Skill Gaps**: What technical competencies are most in-demand, and where do we fall short?
- **Remote Work Trends**: How does remote work status affect salary distributions?

### Key Findings

| Finding | Value |
|---------|-------|
| **AI Wage Premium** | AI roles earn ~14% more ($128,837.87 vs $113,127.44) |
| **Highest AI Premium Regions** | South Dakota & New Mexico (up to 42% premium) |
| **Critical Tech Skills** | Python (95%), SQL (88%), Machine Learning (75%) |
| **Dataset Size** | 72,498 job postings |
| **Usable Salary Records** | 39,244 (after imputation) |
| **Model R² Score** | 0.269 (Multiple Linear Regression) |

---

## 📁 Project Structure
ad688-employability-sp25A1-groupC/ 
├── index.qmd # Project home page & executive summary 
├── introduction.qmd # Research introduction & context 
├── data_cleaning.qmd # Data preparation & cleaning pipeline 
├── eda.qmd # Exploratory Data Analysis 
├── skill_gap_analysis.qmd # Skill demand vs. team capability analysis 
├── salary_analysis.qmd # Salary & compensation trends 
├── ml_methods.qmd # Predictive modeling with MLR and RF
├── career_plan.qmd # Career strategy & upskilling roadmap 
├── _quarto.yml # Quarto configuration 
├── requirements.txt # Python dependencies 
├── references.bib # Bibliography 
├── styles.css # Custom styling 
└── docs/ # Generated HTML output


### Key Quarto Files

| File | Purpose |
|------|---------|
| `index.qmd` | Landing page with project highlights and executive summary |
| `introduction.qmd` | Research motivation and expected findings |
| `data_cleaning.qmd` | Data pipeline: 72,498 → 39,244 usable salary records |
| `eda.qmd` | Geographic & industry clustering, remote work analysis |
| `skill_gap_analysis.qmd` | Market skill demand vs. team capabilities |
| `salary_analysis.qmd` | AI wage premium, regional variations, remote work dividends |
| `ml_methods*.qmd` | Predictive modeling: MLR, alternative approaches, Random Forest |
| `career_plan.qmd` | Phased upskilling strategy to close skill gaps |

---

## 🔧 Technology Stack

### Languages & Frameworks
- **Python** - Core data analysis
- **Quarto** - Document generation & publishing
- **PySpark** - Large-scale data processing


See `requirements.txt` for the complete dependency list.

---

## 📚 Analysis Highlights

### 1. **Data Preparation**
- Cleaned 72,498 raw job postings
- Removed missing/duplicate IDs and trimmed whitespaces
- Implemented **Industry-Median Imputation** strategy for missing salaries
- Expanded usable salary sample from 32,394 to **39,244 records** (21% improvement)

### 2. **Exploratory Data Analysis**
- **Top States:** Texas and California lead in job posting concentration
- **Dominant Sectors:** Finance, Technology, Healthcare
- **Remote Work Insights:** 78.1% of postings lack explicit remote-work tags
- Geographic and industry clustering patterns identified

### 3. **Salary & Compensation Trends**
- **AI Premium Verified:** AI roles command 14% higher average salary
- **Regional Leaders:** South Dakota & New Mexico show up to 42% AI salary premiums
- **Remote Work Dividend:** Remote positions show higher median salaries

### 4. **Skill Gap Analysis**
- **Market Baselines:** Python (95%), SQL (88%), ML (75%)
- **Team Deficits:** 
  - Python: -2.25 (critical gap)
  - Machine Learning: -2.00
  - SQL: -1.90
- High-priority upskilling recommendations identified

### 5. **Predictive Modeling**
- **Multiple Linear Regression and Random Forest** model built with PySpark ML
- **Best R² Score (RF):** 0.566 (predicting salary from occupation, job title, skills, education level among other features)
- **Key Insight:** Entry-level titles show -$61k to -$75k salary penalties
- Years of experience is a significant predictor of compensation

### 6. **Career Strategy**
- Phased upskilling roadmap to bridge identified skill gaps
- Short-term focus: Python, SQL, collaborative tools
- Long-term development: Machine Learning, advanced analytics

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- [Quarto CLI](https://quarto.org/docs/get-started/)
- pip or poetry for package management

### Installation
### Clone the repository
`git clone https://github.com/hanachen-tech/ad688-employability-sp25A1-groupC.git`

`cd ad688-employability-sp25A1-groupC`

### Option 1: Using pip
`pip install -r requirements.txt`

### Option 2: Using poetry
`poetry install`

### Install Quarto CLI (if not already installed)
See: https://quarto.org/docs/get-started/

### Render all Quarto documents
`quarto render`

### Render a specific document
`quarto render index.qmd`

### Preview in browser
`quarto preview`
