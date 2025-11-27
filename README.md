# AI-Based Intrusion Detection System (IDS)

This repository contains an AI-powered **Intrusion Detection System (IDS)** that uses **Machine Learning–based Anomaly Detection** to identify suspicious or abnormal activity in system logs.  
The entire project is implemented in **Google Colab** and stored in the notebook:

**IntrusionDetectionSystem.ipynb**

---

## Project Overview

Traditional intrusion detection tools rely on fixed signatures, which fail to detect new or unknown threats.  
This project solves that by using **anomaly detection**, enabling the system to identify unusual patterns in log data even without predefined rules.

The system:

✔ Loads and preprocesses log data  
✔ Trains an anomaly detection model  
✔ Generates predictions on suspicious events  
✔ Visualizes anomalies for easier understanding  

---

## Features

- **Machine Learning–based anomaly detection**  
- Works on structured log data (CSV logs)  
- Automatically identifies abnormal patterns  
- Uses algorithms like:  
  - `IsolationForest`  
  - `Local Outlier Factor (LOF)`  
- Includes **data preprocessing**, **feature scaling**, and **visualization**  
- Notebook-based pipeline — simple to understand and replicate  
- Runs entirely in **Google Colab**

---

## Technologies Used

| Component | Technology |
|----------|------------|
| Language | Python |
| ML Framework | Scikit-learn |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib |
| Platform | Google Colab |

---

## Project Structure

```
AI-Based-Intrusion-Detection-System-IDS-/
│── IntrusionDetectionSystem.ipynb   # Main project notebook
│── README.md                        # Project documentation
```

(If you later add datasets, models, or screenshots, create folders such as `/data`, `/models`, `/screenshots`.)

---

## How to Run This Project

### **Option 1 — Run in Google Colab (Recommended)**  
1. Open the notebook in Colab  
2. Upload your log file (CSV format recommended)  
3. Run all cells  
4. The notebook will:  
   - preprocess your data  
   - train the anomaly detection model  
   - display anomalous vs normal entries  
   - show graphs of the results  

### **Option 2 — Run Locally (Advanced Users)**  
Install required dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib
```

Then open the notebook using Jupyter:

```bash
jupyter notebook IntrusionDetectionSystem.ipynb
```

---

## Output & Results

The notebook provides:

- Cleaned and preprocessed dataset  
- Trained anomaly detection model  
- A new column marking each log entry as:  
  - **1 = Normal**  
  - **-1 = Anomaly / Suspicious Activity**  
- Graphs showing:  
  - Anomaly distribution  
  - Model decisions  
  - Log patterns  

These outputs help visualize possible intrusion attempts.

---

## Machine Learning Model Used

The IDS uses **unsupervised learning**, meaning it does not require labeled attacks.  
Models used:

### 🔹 Isolation Forest  
- Detects anomalies by isolating data points  
- Very effective for intrusion data

### 🔹 Local Outlier Factor (optional in code)  
- Measures local deviation of a data point  
- Useful for density-based anomaly detection

Both models are implemented using **scikit-learn**.

---

## Future Improvements

- Integrate OSSEC log ingestion  
- Real-time monitoring (live data streaming)  
- Web dashboard for alerts  
- Save & load trained model (`.pkl` export)  
- Add more ML models for better accuracy  
- Deploy the IDS as an API or microservice  

---

## Author

**Devanshu Dangi**   
(GitHub: `dangi21`)

---

## License

This project is open-source and free to use for learning and research.

