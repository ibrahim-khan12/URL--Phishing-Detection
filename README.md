# Url-Phishing-Detection
A machine learning project for analyzing and detecting phishing URLs using feature engineering, pattern recognition, and data exploration.

# 🛡️ URL Phishing Detection Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Machine Learning](https://img.shields.io/badge/ML-Analysis-green.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Processing-orange.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)

A comprehensive machine learning analysis project for detecting phishing URLs through feature engineering and pattern recognition.

## 📋 Project Overview

This project performs an end-to-end analysis of URL phishing detection, implementing data exploration, cleaning, feature engineering, and pattern testing to identify malicious URLs. The analysis follows a structured methodology to prepare data for machine learning applications.

## 🚀 Key Features

- **Data Exploration**: Comprehensive analysis of phishing vs clean URL distributions
- **Feature Engineering**: Creation of 6+ specialized features including:
  - URL length analysis
  - IP address detection
  - TLD classification
  - Subdomain counting
  - Combined feature creation
- **Pattern Testing**: Validation of hypotheses about phishing URL characteristics
- **Data Cleaning**: Robust handling of messy URLs and anomalies

## 🛠️ Methodology

### 1. Data Exploration
- Analyzed class balance between phishing and clean URLs
- Visualized distributions of URL lengths, TLS usage, and domain age
- Manual inspection of sample URLs for pattern identification

### 2. Data Cleaning
- URL parsing to extract domain, path, and query components
- Anomaly detection and handling strategies
- Structured data preparation for feature engineering

### 3. Feature Engineering
- **Boolean Features**: IP address presence, unusual TLD detection
- **Numeric Features**: URL length, subdomain count, path depth
- **Categorical Features**: TLS usage, query string presence
- **Combined Features**: Multiplicative feature engineering (length × subdomain count)

### 4. Pattern Analysis
- Hypothesis testing on URL length claims
- Domain age analysis for legitimacy patterns
- Feature separation analysis between classes

## 📊 Key Insights

1. **Class Imbalance**: Dataset shows slight imbalance with more phishing URLs
2. **Length Patterns**: Phishing URLs tend to be longer due to obfuscation techniques
3. **TLS Adoption**: Both phishing and clean URLs commonly use TLS
4. **Domain Characteristics**: Unusual TLDs and excessive subdomains correlate with phishing
5. **Combined Features**: Multiplicative features show better class separation

## 📊 Sample Results

### Class Distribution
```
phishing    540
clean       460
Name: Verdict, dtype: int64
Balanced: True
```

### Feature Comparison
- **Phishing URLs tend to be longer**:  
  Average phishing URL length is higher than clean URLs.
- **TLS Usage**:  
  Both phishing and clean URLs commonly use TLS.
- **Unusual TLDs**:  
  Phishing URLs more frequently use uncommon TLDs.

### Combined Feature Separation
- The combined feature `url_length × subdomain_count` shows better class separation:
  - Phishing URLs have higher values for this feature.

### Pattern Testing
- **Claim:** "Phishing URLs are always longer than clean ones."
  ```
  Min phishing length: 34
  Max clean length: 120
  Claim holds: False
  ```
- **Claim:** "Older domains are always clean."
  ```
  Any phishing in oldest? False
  ```

### Example URLs
- **Phishing:**  
  - `http://192.168.1.1/login.php?user=abc`
  - `https://secure-paypal.com.verify.account.ru/secure`
- **Clean:**  
  - `https://www.microsoft.com/en-us`
  - `https://www.harvard.edu/academics`

## 🔧 Technical Implementation

```python
# Key libraries used
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from urllib.parse import urlparse
import re
```

### Feature Engineering Pipeline
- URL parsing and component extraction
- Boolean flag creation for suspicious patterns
- Numeric metric calculation
- Combined feature synthesis

## 📈 Results & Findings

- **Pattern Validation**: Tested claims about phishing URL characteristics
- **Feature Effectiveness**: Demonstrated improved class separation with engineered features
- **Data Quality**: Successfully handled anomalies and prepared clean dataset for ML
- **Insights Generation**: Identified key indicators for phishing detection

## 🏗️ Project Structure

```
├── 22I-1755_A1_CY-B.ipynb    # Main analysis notebook
├── url_dataset.csv           # Dataset (not included)
├── README.md                 # This file
└── requirements.txt          # Dependencies
```

## 🚦 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Usage
1. Clone the repository
2. Ensure you have the URL dataset (`url_dataset.csv`)
3. Open and run the Jupyter notebook
4. Follow the step-by-step analysis

## 🔮 Future Enhancements

### Proposed Features
- **Click Rate Analysis**: Monitor URL click patterns in early detection windows
- **Real-time Processing**: Implement streaming data analysis
- **Advanced NLP**: Apply text analysis to URL components
- **Ensemble Methods**: Combine multiple detection approaches

### Evasion Considerations
- Shorter URL generation by attackers
- Domain aging strategies
- Common TLD usage for legitimacy

## 📝 Assignment Compliance

This project addresses all required components:
- ✅ Part A: Comprehensive data exploration
- ✅ Part B: Systematic data cleaning
- ✅ Part C: Strategic feature engineering
- ✅ Part D: Hypothesis-driven pattern testing
- ✅ Part E: ML preparation and justification
- ✅ Part F: Critical reflection and future considerations

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements. Areas for contribution:
- Additional feature engineering techniques
- Advanced visualization methods
- Model implementation and evaluation
- Performance optimization

## 📄 License

This project is part of an academic assignment and is provided for educational purposes.

---

**Author**: M.ibrahim

