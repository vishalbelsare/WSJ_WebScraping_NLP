# Project Objectives

## Primary Research Goals

### 1. Sentiment-Engagement Relationship Analysis
**Objective**: Investigate whether article sentiment characteristics influence reader engagement on Wall Street Journal articles.

**Specific Aims**:
- Determine if subjective vs. objective writing style correlates with comment volume
- Analyze the relationship between positive/negative sentiment and reader engagement
- Identify which sentiment metrics (VADER vs. TextBlob) provide better predictive power
- Quantify the statistical significance of sentiment-engagement relationships

**Success Metrics**:
- Statistical significance testing (p < 0.05)
- Model performance evaluation (R², adjusted R²)
- Identification of key sentiment variables driving engagement

### 2. Market Prediction Analysis
**Objective**: Explore whether WSJ article sentiment can predict S&P 500 market movements.

**Specific Aims**:
- Test predictive power of same-day sentiment on same-day market returns
- Analyze lagged effects (1-3 day prediction windows)
- Compare different sentiment analysis approaches for market prediction
- Control for market volume and other confounding variables

**Success Metrics**:
- Statistical significance of sentiment variables in market prediction models
- Model performance comparison across different time horizons
- Identification of optimal sentiment indicators for market prediction

## Technical Objectives

### 3. Data Collection & Processing
**Objective**: Build a robust web scraping and data processing pipeline.

**Specific Aims**:
- Scrape comprehensive article metadata from WSJ archives
- Implement reliable data cleaning and preprocessing workflows
- Ensure data quality and consistency across the dataset
- Create reproducible data collection processes

**Success Metrics**:
- Complete dataset of 20,000+ articles
- High data quality (minimal missing values, consistent formatting)
- Reproducible scraping pipeline

### 4. Natural Language Processing Implementation
**Objective**: Apply state-of-the-art NLP techniques for sentiment analysis.

**Specific Aims**:
- Implement VADER sentiment analysis for emotion intensity scoring
- Apply TextBlob for polarity and subjectivity analysis
- Compare and validate different NLP approaches
- Create comprehensive sentiment feature engineering

**Success Metrics**:
- Successful implementation of both VADER and TextBlob
- Consistent sentiment scoring across the dataset
- Validation of sentiment analysis accuracy

### 5. Statistical Analysis & Modeling
**Objective**: Conduct rigorous statistical analysis to test research hypotheses.

**Specific Aims**:
- Perform linear regression analysis for engagement prediction
- Implement time-series analysis for market prediction
- Apply appropriate statistical tests and model validation
- Control for confounding variables and bias

**Success Metrics**:
- Properly specified statistical models
- Appropriate handling of statistical assumptions
- Clear interpretation of results and limitations

## Methodological Objectives

### 6. Reproducible Research
**Objective**: Ensure all analysis is fully reproducible and well-documented.

**Specific Aims**:
- Create clear documentation for all analysis steps
- Implement version control for code and data
- Provide detailed methodology descriptions
- Share code and data where appropriate

**Success Metrics**:
- Complete code documentation
- Reproducible analysis notebooks
- Clear methodology documentation

### 7. Interactive Visualization
**Objective**: Create user-friendly interfaces for exploring results.

**Specific Aims**:
- Develop R Shiny dashboard for interactive analysis
- Create visualizations for sentiment trends and patterns
- Enable user exploration of specific articles and time periods
- Provide intuitive data exploration tools

**Success Metrics**:
- Functional interactive dashboard
- Clear and informative visualizations
- User-friendly interface design

## Research Questions

### Primary Questions
1. **Engagement Question**: Does article sentiment (subjectivity, polarity, emotionality) significantly predict the number of comments posted on WSJ articles?

2. **Market Question**: Can WSJ article sentiment on day t predict S&P 500 returns on day t + n (where n = 0, 1, 2, 3)?

### Secondary Questions
3. **Sentiment Comparison**: Which sentiment analysis approach (VADER vs. TextBlob) provides better predictive power for engagement and market movements?

4. **Temporal Patterns**: Are there temporal patterns in sentiment that correlate with market volatility or reader engagement?

5. **Content Analysis**: Do certain types of articles (by section, author, or topic) show stronger sentiment-engagement or sentiment-market relationships?

## Expected Outcomes

### Positive Outcomes
- Identification of significant sentiment-engagement relationships
- Discovery of predictive sentiment patterns for market movements
- Development of robust NLP analysis pipeline
- Creation of valuable dataset for future research

### Potential Limitations
- Limited predictive power due to market complexity
- Potential confounding variables not controlled for
- Temporal limitations of the dataset (2019-2020)
- Possible selection bias in comment engagement

## Success Criteria

### Minimum Viable Results
- Complete data collection and processing pipeline
- Successful implementation of sentiment analysis
- Statistical analysis of both research questions
- Basic visualization and reporting of results

### Optimal Results
- Statistically significant findings for at least one research question
- Strong model performance (R² > 0.1) for engagement prediction
- Identification of actionable insights for content strategy
- Publication-quality analysis and documentation

## Timeline & Milestones

### Phase 1: Data Collection (Weeks 1-2)
- Set up web scraping infrastructure
- Collect initial dataset
- Implement data cleaning and preprocessing

### Phase 2: NLP Implementation (Weeks 3-4)
- Implement VADER and TextBlob analysis
- Create sentiment feature engineering pipeline
- Validate sentiment analysis results

### Phase 3: Statistical Analysis (Weeks 5-6)
- Conduct engagement prediction analysis
- Perform market prediction analysis
- Apply appropriate statistical tests

### Phase 4: Visualization & Reporting (Weeks 7-8)
- Develop R Shiny dashboard
- Create comprehensive visualizations
- Document findings and methodology
- Prepare final report and presentation
