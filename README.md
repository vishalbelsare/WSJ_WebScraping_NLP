# WSJ Web Scraping & NLP Analysis

A comprehensive analysis of Wall Street Journal articles to investigate relationships between article sentiment, reader engagement, and financial market movements.

## Table of Contents

- [Project Overview](#project-overview)
- [Research Questions](#research-questions)
- [Data Collection](#data-collection)
- [Natural Language Processing](#natural-language-processing)
- [Research Findings](#research-findings)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Docker Setup](#docker-setup)
- [Results & Applications](#results--applications)

## Project Overview

This project investigates the relationship between Wall Street Journal article sentiment and two key metrics:
- **User engagement** (measured by comment count)
- **S&P 500 market returns**

The analysis leverages web scraping and natural language processing to extract insights from 22,772 WSJ articles published between January 2019 and July 2020.

## Research Questions

1. **Comment Engagement Analysis**: Can a statistically significant relationship be demonstrated between a WSJ article's degree of subjectivity/objectivity and positivity/negativity in its writing and the number of online comments posted by readers?

2. **Market Prediction Analysis**: Can a statistically significant relationship be demonstrated between WSJ articles' sentiment polarity on day t and S&P 500 Index movements on day t + n (where 0 ≤ n ≤ 3)?

## Data Collection

- **Source**: Wall Street Journal [news archives](https://www.wsj.com/news/archive/years)
- **Method**: Python Selenium web scraping
- **Dataset**: 22,772 full-text articles (Jan 2019 - July 2020)
- **Data Points per Article**:
  - Article text and headline
  - Sub-headline and publication date
  - Author name and rubric category
  - Number of comments

## Natural Language Processing

### Libraries Used
- **VADER** (Valence Aware Dictionary and sEntiment Reasoner)
- **TextBlob**

### VADER Analysis
- **Purpose**: Polarity and emotion intensity scoring
- **Output Variables**: `negative`, `neutral`, `positive`, `compound`
- **Documentation**: [VADER Sentiment](https://pypi.org/project/vaderSentiment/)

### TextBlob Analysis
- **Purpose**: Sentiment analysis and subjectivity scoring
- **Output Variables**: `polarity`, `subjectivity`
- **Documentation**: [TextBlob Documentation](https://textblob.readthedocs.io/en/dev/)

## Research Findings

### Comment Engagement Results
- **Model Performance**: Simple linear regression shows poor predictive power (Adj R² = 0.014)
- **Statistical Significance**: Cannot reject null hypothesis (p-value = 0.2045)
- **Key Finding**: VADER negativity scores are statistically significant at 1% level
- **Interpretation**: Higher negativity may correlate with events generating public response (e.g., public figure deaths)

### Market Prediction Results
- **Model Performance**: Low predictive power across all models (Adj R² ≈ 0.01)
- **Analysis Scope**: Four regression models testing same-day and next-day S&P 500 movements
- **Key Finding**: TextBlob polarity shows significance at 10% level
- **Conclusion**: WSJ sentiment has limited predictive power for market movements

## Project Structure

```
WSJ_WebScraping_NLP/
├── app/                    # R Shiny application
│   ├── global.R
│   ├── server.R
│   └── ui.R
├── data/                   # Processed datasets
│   └── wsjsections.csv
├── notebooks/              # Jupyter analysis notebooks
│   └── WSJ_Scraping NLP_Analysis.ipynb
├── scraping/               # Web scraping scripts
│   └── scrape.py
├── Dockerfile             # Container configuration
├── README.md              # Project documentation
└── objectives.md          # Detailed project objectives
```

## Getting Started

### Prerequisites
- Python 3.9+
- R (for Shiny app)
- Docker (optional)

### Local Setup
1. Clone the repository
2. Install Python dependencies: `pip install -r requirements.txt`
3. Run the Jupyter notebook for analysis
4. Launch R Shiny app for interactive visualization

## Docker Setup

### Building the Container
```bash
docker build -t wsj-nlp-analysis .
```

### Running the Container
```bash
docker run -p 8888:8888 wsj-nlp-analysis
```

### Accessing the Application
- Open your browser and navigate to `http://localhost:8888`
- The Jupyter notebook interface will be available
- Use the provided token for authentication

### Stopping the Container
```bash
docker stop <container_id>
```

## Results & Applications

### Interactive Dashboard
- **R Shiny App**: [Live Application](https://philippe1.shinyapps.io/WSJApp2/)
- **Features**: Interactive sentiment analysis visualization and data exploration

### Documentation
- **Blog Post**: [Detailed Analysis](https://nycdatascience.com/blog/student-works/scraping-wall-street-journal-article-data-to-measure-online-reader-engagement-an-nlp-analysis/)
- **Objectives**: See `objectives.md` for detailed project goals and methodology

