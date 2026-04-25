# Pattern_Recognition
# Discount Signals vs. Satisfaction
### Multimodal Prediction of Ratings and Sentiment on Amazon Product Listings

**Author:** Sidra Farooqui  
**Course:** CAP 5638 — Pattern Recognition — Spring 2026  
**University:** Florida State University

---

## Project Overview

This project investigates whether numeric discount signals (percentage, absolute markdown, price ratio) combined with review text can predict customer satisfaction on Amazon product listings. Three research questions are addressed:

- **RQ1:** Can we predict star ratings (1–5) from discount signals + review text? (Regression)
- **RQ2:** Does adding pricing context improve sentiment classification? (Classification)
- **RQ3:** Does the discount–satisfaction relationship vary by product segment? (Clustering)

---

## How to Run the Code

### Prerequisites

- Python 3.10 or higher
- Google Colab (recommended) or any Jupyter environment

### Step-by-Step Instructions

1. **Download the dataset:**
   - Amazon Sales Dataset from Kaggle: https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset
   - Direct download: click "Download" on the Kaggle page, extract the CSV file

2. **Open the notebook:**
   - Upload `SidraFarooqui_PatternRecognitionProject.ipynb` to Google Colab
   - Or open it in Jupyter Notebook / JupyterLab locally

3. **Upload the dataset:**
   - In Colab: click the folder icon in the left sidebar, then upload `amazon.csv`
   - Locally: place `amazon.csv` in the same directory as the notebook

4. **Run the entire notebook:**
   - In Colab: click **Runtime → Run All**
   - Locally: click **Cell → Run All**
   - One trigger runs the whole code in sequence without any disruption

5. **Wait for completion:**
   - Estimated time: **~2 minutes** on standard Colab CPU
   - Progress indicators print at each stage (e.g., "Rating regression baseline complete", "Clustering complete")
   - The final output prints **"Project complete"** with a full results summary table

---

## File Structure

```
├── README.md                                            # This file
├── SidraFarooqui_PatternRecognitionProject.ipynb         # Complete notebook (all code)
├── amazon.csv                                            # Dataset (download from Kaggle link above)
├── CAP5638_Final_Report_Farooqui_FINAL.docx              # Project report
└── Discount_Signals_Presentation_Editorial.pptx          # Presentation slides
```

---

## Libraries Used

| Library        | Version  | Purpose                                    |
|----------------|----------|--------------------------------------------|
| Python         | 3.10+    | Runtime                                    |
| numpy          | 1.24+    | Numerical computation                      |
| pandas         | 2.0+     | Data loading and manipulation              |
| scikit-learn   | 1.4+     | ML models, preprocessing, metrics, clustering |
| xgboost        | 2.0.3    | Gradient boosting models (XGBRegressor, XGBClassifier) |
| matplotlib     | 3.7+     | Visualization (charts, scatter plots)      |
| seaborn        | 0.12+    | Statistical plots (heatmap, confusion matrix) |
| scipy          | 1.10+    | ANOVA statistical test (f_oneway)          |
| shap           | 0.43.0   | (installed but optional — for future interpretability work) |

All libraries are installed automatically in the first cell of the notebook via:
```
!pip -q install shap==0.43.0 xgboost==2.0.3
```
All other libraries come pre-installed in Google Colab.

For local installation:
```bash
pip install numpy pandas scikit-learn xgboost matplotlib seaborn scipy shap
```

---

## Code Structure (Sequential Execution)

The notebook runs sequentially. One trigger (Run All) executes everything from data loading to final results:


## Dataset

- **Name:** Amazon Sales Dataset
- **Source:** Kaggle
- **URL:** https://www.kaggle.com/datasets/karkavelrajaj/amazon-sales-dataset
- **Size:** 1,465 rows x 16 columns
- **Fields used:** actual_price, discounted_price, discount_percentage, rating, review_content, review_title, category, product_id
- **License:** Available under Kaggle's dataset terms of use


## Contact

Sidra Farooqui — Florida State University  
GitHub: https://github.com/SidraFarooqui/Pattern_Recognition_Project_Amazon-Discounts-vs.-Satisfaction
