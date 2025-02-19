# Phishing URL Detection System

A machine learning-based solution to detect phishing URLs by analyzing URL characteristics and domain reputation.

## Overview

This project implements a phishing URL detection system that helps users identify potentially malicious websites. It uses machine learning techniques to analyze various URL features and determines if a URL is likely to be safe or a phishing attempt.

## Features

- Extracts 20+ features from URLs for comprehensive analysis
- Leverages domain reputation data from top-ranked websites
- Provides both command-line and web-based interfaces
- Achieves high accuracy in distinguishing legitimate from phishing sites
- Computes confidence scores for predictions

## Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn
- XGBoost-1.5+
- tldextract
- matplotlib
- seaborn
- gradio (optional, for web interface)

## Quick Start

1. Clone this repository:
   ```
   git clone https://github.com/Darshit1617/phishing-url-detection.git
   cd Phishing_domain_detectot
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the python notebook via Google Colab:

4. Follow the instructions in the notebook to:
   - Load datasets
   - Extract features
   - Train the model
   - Make predictions

## Usage

### Command-line Interface

```python
# After training the model:
check_url_safety()
```

Example:
```
Enter a URL to check (or 'exit' to quit): facebook.com
URL: http://facebook.com
✅ The URL is safe.
Confidence: 96.45%
```

### Web Interface (Optional)

```python
# Launch the Gradio interface after training:
iface.launch()
```

## Data

The system requires two datasets:
1. **Ranked domains** - A list of top legitimate domains
2. **Phishing URLs** - A labeled dataset with good and bad URLs

Sample data format for phishing URLs:
```
URL,Label
https://www.google.com,good
http://paypal-secure.phishing-example.com,bad
```

## Model Performance

- Accuracy: 83.83%+ (depending on dataset quality)
- ROC-AUC: 0.91+

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
