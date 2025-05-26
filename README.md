# AI-Powered-Student-Exam-Performance-Predictor


This project is a **Streamlit dashboard** that predicts whether students will **pass or fail** based on their outcome scores using a machine learning model (XGBoost). It features interactive controls, clean visualizations, and Excel export functionality.

Note: This is a prototype version of the dashboard and model. It is still under active development and may require further improvements for production-level use.


---
## Screenshot
![AI powered](https://github.com/user-attachments/assets/e7c4e5a7-f71a-4df2-b485-5827930e1a07)


---

## Features

* Upload Excel files with student performance data
*  Adjustable pass mark threshold (via sidebar)
*  Trains an XGBoost classification model
*  Prediction results dashboard:

  * Pass/fail distribution
  * Probability histogram
  * Feature importance bar chart
*  Download predicted results as Excel file
*  Styled layout with metric cards and sidebar filters

---

##  Technologies Used

* Python 3.8+
* Streamlit
* Pandas
* XGBoost
* Seaborn & Matplotlib
* Joblib
* openpyxl

---

##  Project Structure

```
.
├── app.py                # Main Streamlit application
├── predictions.xlsx      # Generated results file (after prediction)
├── model.pkl             # Saved ML model
├── README.md             # Project documentation
├── requirements.txt      # Python dependencies
└── screenshot.png        # Dashboard screenshot
```

---

## Sample Excel Input Format

Ensure your Excel file follows this format:

| Student ID | Outcome1 | Outcome2 | Outcome3 | Total Mark |
| ---------- | -------- | -------- | -------- | ---------- |
| 10001      | 12       | 18       | 15       | 45         |
| 10002      | 4        | 6        | 7        | 17         |

**Required Columns:**

* At least one `Outcome` column (e.g., Outcome1, Outcome2, ...)
* A `Total Mark` column
* A `Student ID` column (for result tracking)

---


## Usage

1. Upload your Excel file containing student performance data.
2. Adjust the "Pass Threshold" slider if needed.
3. Click "Retrain Model" to build a new prediction model.
4. View metrics and visualizations on screen.
5. Download the results using the "Download" button.
