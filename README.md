# Safelink Detection

Safelink Detection is a web-based application designed to identify malicious URLs using machine learning and real-time feature extraction. The system utilizes a Flask backend, a trained Gradient Boosting model, and a custom feature extraction engine to analyze the structure, behavior, and metadata of URLs.

---

## How It Works

1. **User Input:** The user provides a URL through the web interface.
2. **Feature Extraction:** Features are extracted from the URL, including WHOIS information, domain structure, and content analysis.
3. **Classification:** A trained Gradient Boosting model classifies the URL as Safe or Malicious.
4. **Results:** The system displays the classification result and a confidence score to the user.

---

## Features Extracted

The project extracts 30 distinct features to ensure accurate detection, including:

*   IP Address presence in URL
*   URL and Domain length analysis
*   Shortened URL detection (e.g., bit.ly, tinyurl)
*   Presence of @ symbols and redirect patterns
*   HTTPS availability
*   WHOIS data (domain age, registration length)
*   JavaScript-based anomaly detection (popups, status bar spoofing)
*   Google Index status
*   Alexa Rank verification
*   DNS and traffic validation
*   Suspicious TLD and IP block checking

All feature extraction logic is implemented in `feature.py`.

---

## Frontend

*   Responsive HTML/CSS interface.
*   Intuitive URL input field.
*   Clear display of safety status (Safe or Unsafe).
*   Visual styling powered by custom CSS.

---

## Technical Overview

The project demonstrates the effectiveness of machine learning in cybersecurity. Through rigorous testing and model comparison, the Gradient Boosting Classifier was identified as the top-performing model with an accuracy of 97.4%, outperforming alternatives like CatBoost and Random Forest.

